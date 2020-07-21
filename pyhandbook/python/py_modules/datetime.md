# DateTime Module

```python
import datetime
import pytz

d = datetime.date(2016, 7, 24)
# dont write 7 as 07, it will return error

tdelta = datetime.timedelta(days = 7)
print(tdelta) # 7 days, 0:00:00

# date1 +- date2 = timedelta
# timedelta +- date1 = date2

tday = datetime.date(2018, 9, 15)
tday.day
tday.month
tday.year
tday.weekday() # monday == 0
tday.isoweekday() # monday == 1

t = datetime.time(9, 30, 45, 10000)
t.hour
t.minutes
t.seconds

dt = datetime.datetime(2016, 7, 26, 12, 30, 45, 100000)
dt.date()
dt.time()
dt.day
dt.minute


dt_today = datetime.datetime.today()
# returns local time
dt_now = datetime.datetime.now(tz=pytz.UTC)
# returns local time but we can provide timezone
dt_utcnow = datetime.datetime.utcnow()
```

**Note:** Don’t name your .py file as 'datetime' or any other module you are importing.