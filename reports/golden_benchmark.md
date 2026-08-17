# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **1165.0 ms**
- Average token reduction vs full source context: **14.5%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.3 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| G06 | long_term | PASS | 1751.6 | 878 | 0.0% |  |
| G09 | semantic | PASS | 282.3 | 148 | 67.8% |  |
| G10 | semantic | PASS | 275.1 | 95 | 79.3% |  |
| G14 | mixed | PASS | 1743.4 | 431 | 0.0% |  |
| G03 | long_term | PASS | 1439.7 | 1520 | 0.0% |  |
| G04 | long_term | PASS | 1491.9 | 1522 | 0.0% |  |
| G07 | episodic | PASS | 450.3 | 629 | 0.0% |  |
| G08 | episodic | PASS | 266.6 | 604 | 0.0% |  |
| G11 | mixed | PASS | 1730.1 | 439 | 22.3% |  |
| G13 | mixed | PASS | 579.4 | 406 | 28.1% |  |
| G15 | mixed | PASS | 1988.5 | 736 | 0.0% |  |
| G16 | mixed | PASS | 1819.1 | 484 | 14.3% |  |
| G17 | mixed | PASS | 1831.5 | 484 | 14.3% |  |
| G18 | mixed | PASS | 603.5 | 403 | 28.7% |  |
| G19 | mixed | PASS | 1842.8 | 581 | 0.0% |  |
| G05 | long_term | PASS | 1598.6 | 1510 | 0.0% |  |
| G12 | mixed | PASS | 1800.1 | 431 | 31.8% |  |
| G20 | mixed | PASS | 1805.4 | 609 | 3.6% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G06 - long_term

`FACT: Da hieu provides backend examples. [valid_at=2026-08-01T11:00:20Z, invalid_at=None] FACT: Lan Tran does not use Python in the LOTUS-88 project backend. [valid_at=2026-08-01T11:00:00Z, invalid_at=None] FACT: Lan Tran's project is LOTUS-88. [valid_at=2026-08-01T11:00:00Z, invalid_at=2026-08-01T11:00:20Z] FACT: Lan Tran prioritizes Spring Boot for the LOTUS-88 project. [valid_at=2026-08-01T11:00:00Z, invalid_at=None] FACT: Lan Tran prioritizes Java for the LOTUS-88 project. [valid_at=2026-08-01T11:00:00Z, invalid_at=None] FACT: Da hieu uses Spring Boot. [valid_at=2026-08-01T11:00:20Z, invalid_at=None] FACT: Da hieu uses Java. [valid_at=2026-08-01T11:00:20Z, invalid_at=None] FACT: Da hieu `

### G09 - semantic

`EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. EPISODE: Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodic 3 percent, semantic 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3.`

### G10 - semantic

`EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. EPISODE: Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodic 3 percent, semantic 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3.`

### G14 - mixed

`<LONG_TERM> FACT: Lan Tran does not use Python in the LOTUS-88 project backend. [valid_at=2026-08-01T11:00:00Z, invalid_at=None] FACT: Da hieu provides backend examples. [valid_at=2026-08-01T11:00:20Z, invalid_at=None] FACT: Lan Tran's project is LOTUS-88. [valid_at=2026-08-01T11:00:00Z, invalid_at=2026-08-01T11:00:20Z] FACT: Lan Tran prioritizes Spring Boot for the LOTUS-88 project. [valid_at=2026-08-01T11:00:00Z, invalid_at=None] FACT: Lan Tran prioritizes Java for the LOTUS-88 project. [valid_at=2026-08-01T11:00:00Z, invalid_at=None] FACT: The Lab Assistant identifies 'Da hieu' as LOTUS-88. [valid_at=2026-08-01T11:00:20Z, invalid_at=None] FACT: Da hieu uses Spring Boot. [valid_at=2026-08-`

### G03 - long_term

`FACT: demo ca nhan ORCHID-27 prefers Python. [valid_at=2026-08-01T09:00:20Z, invalid_at=2026-08-05T08:00:00Z] FACT: Minh Nguyen likes Python. [valid_at=2026-08-01T09:00:00Z, invalid_at=2026-08-01T09:00:20Z] FACT: Minh Nguyen does not like Java. [valid_at=2026-08-01T09:00:00Z, invalid_at=2026-08-01T09:00:20Z] FACT: Minh Nguyen is learning async/await. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: demo ca nhan ORCHID-27 avoids Java. [valid_at=2026-08-01T09:00:20Z, invalid_at=2026-08-05T08:00:00Z] FACT: Minh Nguyen often confuses Task with coroutine. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen tried to increase the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, `

### G04 - long_term

`FACT: Minh Nguyen often confuses Task with coroutine. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen often confuses coroutine with Task. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen is learning async/await. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen tried to increase the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, invalid_at=2026-08-03T10:03:00Z] FACT: Minh Nguyen has a to-do item to complete the benchmark report by Friday at 16:00. [valid_at=2026-08-01T09:04:00Z, invalid_at=None] FACT: Minh Nguyen requests an explanation using a timeline if this topic (async/await) is encountered later. [valid_at=2026-08-01T09:02:00Z, inv`

### G07 - episodic

`EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHI EPISODE: Minh sap viet script ca nhan de tai hien su co latency, muon code dung ngon ngu minh thich khi lam mot minh, dong thoi bam sat playbook incident cua lab chu dung vo tang timeout. G EPISODE: Toi nay minh`

### G08 - episodic

`EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHI EPISODE: Da tach scope: BLUEBIRD-42 dung TypeScript/NestJS; ORCHID-27 van uu tien Python. EPISODE: Minh sap viet script ca nhan de tai hien su co latency, muon code dung ngon ngu minh thich khi lam mot minh, dong thoi bam sat playbook incident cua lab chu dung vo tang timeout. G EPISODE: Toi nay minh viet tool ca nhan de tai hien su co`

### G11 - mixed

`<LONG_TERM> FACT: Minh Nguyen tried to increase the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, invalid_at=2026-08-03T10:03:00Z] FACT: Minh Nguyen failed to debug async HTTP even after increasing the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, invalid_at=2026-08-03T10:03:00Z] FACT: Minh Nguyen is learning async/await. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen is debugging async HTTP. [valid_at=2026-08-03T10:00:00Z, invalid_at=None] FACT: Minh Nguyen likes Python. [valid_at=2026-08-01T09:00:00Z, invalid_at=2026-08-01T09:00:20Z] FACT: Minh Nguyen often confuses coroutine with Task. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen often confuse`

### G13 - mixed

`<EPISODIC> EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Da tach scope: BLUEBIRD-42 dung TypeScript/NestJS; ORCHID-27 van uu tien Python. EPISODE: Toi nay minh viet tool ca nhan de tai hien su co HTTP roi sua dung playbook. Can ba manh: ngon ngu minh thich khi lam mot minh, ma su co async lan truoc, va buoc playbook truoc khi EPISODE: Minh con mot open-loop phai nop truoc deadline, dong thoi muon ghi chu retry payment dung so lan toi `

### G15 - mixed

`<LONG_TERM> FACT: Minh Nguyen is debugging async HTTP. [valid_at=2026-08-03T10:00:00Z, invalid_at=None] FACT: Minh Nguyen failed to debug async HTTP even after increasing the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, invalid_at=2026-08-03T10:03:00Z] FACT: Minh Nguyen is learning async/await. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen requests an explanation using a timeline if this topic (async/await) is encountered later. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: demo ca nhan ORCHID-27 prefers Python. [valid_at=2026-08-01T09:00:20Z, invalid_at=2026-08-05T08:00:00Z] FACT: Minh Nguyen tried to increase the timeout to 60s. [valid_at=2026-08-03T10:00:0`

### G16 - mixed

`<LONG_TERM> FACT: This benchmark report is an open loop LAB-REPORT-1600. [valid_at=2026-08-01T09:04:00Z, invalid_at=None] FACT: Minh Nguyen is learning async/await. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen has a to-do item to complete the benchmark report by Friday at 16:00. [valid_at=2026-08-01T09:04:00Z, invalid_at=None] FACT: Minh Nguyen tried to increase the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, invalid_at=2026-08-03T10:03:00Z] FACT: Minh Nguyen failed to debug async HTTP even after increasing the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, invalid_at=2026-08-03T10:03:00Z] FACT: Minh Nguyen is debugging async HTTP. [valid_at=2026-08-03T10:00:00Z, i`

### G17 - mixed

`<LONG_TERM> FACT: Minh Nguyen often confuses coroutine with Task. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen often confuses Task with coroutine. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen requests an explanation using a timeline if this topic (async/await) is encountered later. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Coroutine has priority over timeline when explaining coroutine and Task. [valid_at=2026-08-01T09:02:20Z, invalid_at=None] FACT: Minh Nguyen is debugging async HTTP. [valid_at=2026-08-03T10:00:00Z, invalid_at=None] FACT: Minh Nguyen is learning async/await. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Task h`

### G18 - mixed

`<EPISODIC> EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHI EPISODE: Chuan bi demo ca nhan: ten/ma project rieng cua Minh la gi, va lan async HTTP truoc minh reuse client nhu the nao (kem ma su co)? Khong can policy domain chung, chi memory cua Minh EPISODE: Sep hoi chuan hoa backend du an cong ty, minh hay l`

### G19 - mixed

`<LONG_TERM> FACT: Minh Nguyen is debugging async HTTP. [valid_at=2026-08-03T10:00:00Z, invalid_at=None] FACT: Minh Nguyen failed to debug async HTTP even after increasing the timeout to 60s. [valid_at=2026-08-03T10:00:00Z, invalid_at=2026-08-03T10:03:00Z] FACT: Minh Nguyen found that reusing aiohttp ClientSession with concurrency=20 is an effective strategy. [valid_at=2026-08-03T10:03:00Z, invalid_at=2026-08-03T10:03:20Z] FACT: Minh Nguyen is learning async/await. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: Minh Nguyen requests an explanation using a timeline if this topic (async/await) is encountered later. [valid_at=2026-08-01T09:02:00Z, invalid_at=None] FACT: demo ca nhan ORCHI`

### G05 - long_term

`FACT: Minh Nguyen states that Python is not to be used for the backend of the BLUEBIRD-42 project. [valid_at=2026-08-05T08:00:00Z, invalid_at=2026-08-05T08:00:20Z] FACT: Minh Nguyen likes Python. [valid_at=2026-08-01T09:00:00Z, invalid_at=2026-08-01T09:00:20Z] FACT: demo ca nhan ORCHID-27 prefers Python. [valid_at=2026-08-01T09:00:20Z, invalid_at=2026-08-05T08:00:00Z] FACT: Minh Nguyen is updating that for the BLUEBIRD-42 project, the backend must use TypeScript with NestJS. [valid_at=2026-08-05T08:00:00Z, invalid_at=2026-08-05T08:00:20Z] FACT: Minh Nguyen's personal project is ORCHID-27. [valid_at=2026-08-01T09:00:00Z, invalid_at=2026-08-01T09:00:20Z] FACT: Minh Nguyen does not like Java. [`

### G12 - mixed

`<LONG_TERM> FACT: Minh Nguyen is updating that for the BLUEBIRD-42 project, the backend must use TypeScript with NestJS. [valid_at=2026-08-05T08:00:00Z, invalid_at=2026-08-05T08:00:20Z] FACT: Minh Nguyen states that Python is not to be used for the backend of the BLUEBIRD-42 project. [valid_at=2026-08-05T08:00:00Z, invalid_at=2026-08-05T08:00:20Z] FACT: BLUEBIRD-42 is programmed in TypeScript/NestJS. [valid_at=2026-08-05T08:00:20Z, invalid_at=None] FACT: Lab Assistant uses the da tach scope BLUEBIRD-42. [valid_at=2026-08-05T08:00:20Z, invalid_at=None] FACT: Lab Assistant is demoing the demo ca nhan ORCHID-27. [valid_at=2026-08-01T09:00:20Z, invalid_at=2026-08-05T08:00:20Z] FACT: Minh Nguyen'`

### G20 - mixed

`<SHORT_TERM> <SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Filler about dashboard widgets. | assistant: Filler. | user: Filler about CSS variables. | assistant: Filler. | user: Filler about copy review. | assistant: Filler. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler about empty charts. assistant: Filler. user: Filler about telemetry. assistant: Filler. user: Filler about a11y labels. assistant: Filler. </RECENT_TURNS> </SHORT_TERM>`
