# Kusto syntax highlighting

## Initial test

```kusto
Events
| where Name == "Start"
| project City, ClientIp, StartTime = timestamp
| join  kind=inner
    (Events
    | where Name == "Stop"
    | project StopTime = timestamp, ClientIp)
    on ClientIp
| extend duration = StopTime - StartTime
    // Remove matches with earlier stops:
| where  duration > 0
    // Pick out the earliest stop for each start and client:
| summarize argmin(duration, *) by bin(StartTime,1s), ClientIp
```
