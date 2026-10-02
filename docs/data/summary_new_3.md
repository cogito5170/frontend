기준선에서 오류이거나 Claude 도 판정을 못 넘은 프롬프트: [22]

| 팔 | LLM 토큰 합 | 기준선 대비 | 가로챔 | 그중 틀림 | 컴파일 토큰 | 지연 합(s) | 지연 중앙(s) |
|---|---|---|---|---|---|---|---|
| BASE | 1,031,920 | 1.000 | 0 | 0 | 0 | 122.0 | 5.21 |
| WALP | 708,145.0 | 0.686 | 9 | 2 | 0 | 79.5 | 4.23 |
| MBA-0 | 795,941 | 0.771 | 5 | 1 | 0 | 95.8 | 4.40 |
| MBA-1 | 525,277 | 0.509 | 10 | 1 | 24,013 | 167.7 | 8.65 |
| STACK | 339,084 | 0.329 | 16 | 3 | 14,448 | 101.1 | 2.14 |

### 가로챈 프롬프트 (번호:경로, ✗ = 틀림)

- **BASE**: 없음
- **WALP**: 1:WALP:greet, 2:WALP:thanks, 3:WALP:bye, 4:WALP:about_self, 5:WALP:capability, 6:WALP:thanks, 11:WALP:help✗, 12:WALP:help✗, 23:WALP:thanks
- **MBA-0**: 6:cache, 10:cache, 14:cache, 20:cache, 22:cache✗
- **MBA-1**: 6:cache, 7:QUERY, 9:QUERY, 10:QUERY, 11:QUERY, 12:QUERY, 14:cache, 18:QUERY, 20:cache, 22:cache✗
- **STACK**: 1:WALP:greet, 2:WALP:thanks, 3:WALP:bye, 4:WALP:about_self, 5:WALP:capability, 6:WALP:thanks, 7:QUERY, 9:QUERY, 10:QUERY, 11:WALP:help✗, 12:WALP:help✗, 14:cache, 18:QUERY, 20:cache, 22:cache✗, 23:WALP:thanks

### 부류별 가로챔 (가로챔/그 부류 수)

| 팔 | 잡담 | 섞임 | 저장소 질문 | 일반 | 상태 바꿈 |
|---|---|---|---|---|---|
| BASE | 0/7 | 0/2 | 0/5 | 0/8 | 0/2 |
| WALP | 7/7 | 0/2 | 2/5 | 0/8 | 0/2 |
| MBA-0 | 1/7 | 0/2 | 1/5 | 3/8 | 0/2 |
| MBA-1 | 1/7 | 1/2 | 5/5 | 3/8 | 0/2 |
| STACK | 7/7 | 1/2 | 5/5 | 3/8 | 0/2 |
