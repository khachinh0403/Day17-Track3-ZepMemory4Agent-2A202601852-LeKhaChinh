# Lab 17 Submission

## Kết quả và phân tích

Memory-enabled đạt **11/11 (100%)**, cao hơn no-memory **2/11 (18,18%)**; chi tiết nằm trong `reports/comparison.md`. Không có layer yếu nhất riêng lẻ vì short-term, long-term, episodic, semantic và mixed đều đạt 100%. Long-term là layer quan trọng nhất trong bộ test này: nó đóng góp bốn case E02, E03, E08 và E09, đồng thời cung cấp nửa evidence cá nhân cho E07.

E03 retrieve nhiều nhất với **1.521 token**. E07 cần kết hợp long-term (`Python`) với semantic (`Idempotency-Key`); thiếu một trong hai thì hướng dẫn không vừa cá nhân hóa vừa đúng policy payment. Mức giảm token trung bình của memory-enabled là **14,19%**, trong khi no-memory là **81,82%**. Reduction cao của baseline không có nghĩa là tốt: nó tiết kiệm token bằng cách trả rỗng và làm mất evidence, nên chỉ pass hai case short-term.

E08 minh họa recency có scope: BLUEBIRD-42 dùng TypeScript/NestJS, còn preference Python cũ vẫn đúng cho ORCHID-27. E10 cho thấy compaction phải giữ state/constraint; dù raw turn cũ bị evict, durable note vẫn giữ `REVIEW-DEADLINE-1600`, Friday và 16:00.

## Kiến trúc và guardrail

Zep Context Block tự tổng hợp facts liên quan, cross-session recall, provenance và graph validity nên giảm nhiều logic orchestration. Redis + Qdrant cho quyền kiểm soát schema, TTL, ranking, chi phí và nơi lưu dữ liệu, nhưng phải tự xây extraction, user isolation, conflict resolution, deletion và observability.

Để chống memory poisoning, durable write phải qua consent, allowlist loại memory, kiểm tra scope/user, lưu source–timestamp–confidence, và yêu cầu review cho preference/task tác động cao. Fact mới mâu thuẫn không được âm thầm xóa fact cũ: dùng recency + validity và giữ provenance. Retrieval phải giới hạn đúng `user_id`; semantic knowledge chỉ được ghi vào shared graph đã curate. Heartbeat chạy read-only/dry-run mặc định và không được tự cấp quyền.
