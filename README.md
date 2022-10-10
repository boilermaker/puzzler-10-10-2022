# Riddler Express

> A digital 12-hour clock displays 10 digits: two digits representing the hour 
> (from “00” to “12”), two digits representing the minute, 
> two digits representing the second and four digits representing the year.

> When will the clock next use every digit from 0 to 9?

## Lets start with the year.

The first unique occurrence is 2031.  But looking ahead at the hour, we need a digit of 0, or 1 and 2.  2031 knocks out all 3.  In fact 20xx will not work. because that would only leave a 1 for the hour, and we cannot have an hour of 11.  Moving forward we come to 2134.

This looks promising.  Leaving the digits 0, 5, 6, 7, 8, 9 for the hour, minutes seconds.  But then we realize that the minutes and seconds have to start with 0-5. Since the hour will use the 0 digit, that only leaves a 5 for the minutes and seconds.  So we need to revisit our year.  We cannot use 2135 for the same reason that we would only have a single workable digit for the ten's column of the minutes and seconds.

That sets our year to **2136**, leaving 0, 4, 5, 7, 8, 9 available.

## Filling in the ten's column for the hour, minutes, second.

We want to choose the earliest time available, so that would provide:

- hour: 0x
- minute: 4x
- second: 5x.

With 7, 8, 9 remaining

## Putting it all together.

Filling in with the remaining digits, the next instance of the clock using every digit would be:  **07:48:59, 2136**
