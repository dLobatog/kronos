# Introduction to kronos

Kronos uses [Instaparse](https://github.com/Engelberg/instaparse) to generate a parser from a
context-free grammar. This context-free grammar contains a number of symbols that Kronos identifies
as schedule operators. The definition of the grammar, still under construction, is:

```
S := (time-expression | time-unit | preposition)
time-expression := (determiner time-unit preposition time-unit)
time-unit := hour-expression | "hour" | "minute" |  "day" |  "week" |  "month" | "weekday" | "weekend"
preposition := "on" |  "in" |  "at"
determiner := "every" | "each"
hour-expression := (12h-number ("am" | "pm")) | (24h-number)
12h-number := "1" | "2" |  "3" |  "4" |  "5" |  "6" |  "7" | "8" | "9" | "10" | "11" | "12"
24h-number := 12h-number | "13" |  "14" |  "15" |  "16" |  "17" |  "18" |  "19" |  "20" |  "21" |
              "22" |  "23" |  "0"
weekday := 'monday' | 'tuesday' | 'wednesday' | 'thursday' | 'friday' | 'saturday' | 'sunday'
```

Sample sentences (grammar is not finished):
```
  every friday at 5pm
  on tuesdays every hour
  tuesdays every hour
  every hour on tuesdays
  at 5pm on tuesdays in may
  fridays at 5:20am
  fridays at 5:20
  every hour on friday
  tuesdays, fridays at 4am in July
  mondays, wednesdays, fridays at 4am on July 28th
```
