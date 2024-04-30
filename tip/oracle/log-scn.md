---
description: Log의 시작 SCN을 확인할 때 사용한다.
---

# Log의 시작 SCN 확인

{% code fullWidth="false" %}
```sql
SELECT SEQUENCE#, FIRST_CHANGE# FROM V$LOG_HISTORY;
```
{% endcode %}
