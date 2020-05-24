This dataset includes the official statistics on the 11,538 athletes (6,333 men and 5,205 women) and 306 events at the 2016 Olympic Games in Rio de Janeiro. The data was taken from the [Rio 2016 website][rio], which has since been deleted. You can read more about that in a blog post, ["Data for the 2016 Olympic Games in Rio de Janeiro"][blg].

* [Download the athlete data as a CSV][ath]
* [Download the event data as a CSV][evt]

## Column definitions for `athletes.csv`

The athlete data is stored in [`athletes.csv`][ath]; one athlete per row, and eleven columns. Empty cells are null values.

1. `id`
    * Athlete id
    * Integer between 1 and 1,000,000,000
    * Unique
    * No null values
2. `name`
    * Athlete's full name
    * String up to forty characters in length
    * Not unique
    * No null values
3. `nationality`
    * Athlete's nationality
    * One of the [IOC][ioc]'s 206 [three-letter country codes][tcc], or `ROT` for members of the [Refugee Olympic Team][rot]. Kuwaiti athletes' nationality is given as `IOA` due to the [suspension of the Kuwait Olympic Committee][koc]
    * Not unique
    * No null values
4. `sex`
    * Athlete's sex
    * One of two lower-case string values:
        * `male`
        * `female`
    * Not unique
    * No null values
5. `date_of_birth`
    * Athlete's date of birth
    * `YYYY-MM-DD` format
    * Not unique
    * No null values
6. `height`
    * Athlete's height, in metres
    * Floating-point number
    * Not unique
    * Contains null values
7. `weight`
    * Athlete's weight, in kilograms
    * Integer
    * Not unique
    * Contains null values
8. `sport`
    * The sport in which the athlete competes, as defined by the [IOC][ioc]
    * One of 28 lower-case string values
        * `aquatics`
        * `archery`
        * `athletics`
        * `badminton`
        * `basketball`
        * `boxing`
        * `canoe`
        * `cycling`
        * `equestrian`
        * `fencing`
        * `football`
        * `golf`
        * `gymnastics`
        * `handball`
        * `hockey`
        * `judo`
        * `modern pentathlon`
        * `rowing`
        * `rugby sevens`
        * `sailing`
        * `shooting`
        * `table tennis`
        * `taekwondo`
        * `tennis`
        * `triathlon`
        * `volleyball`
        * `weightlifting`
        * `wrestling`
    * Not unique
    * No null values
9. `gold`
    * Number of gold medals won by the athlete
    * Integer
    * Not unique
    * No null values
10. `silver`
    * Number of silver medals won by the athlete
    * Integer
    * Not unique
    * No null values
11. `bronze`
    * Number of bronze medals won by the athlete
    * Integer
    * Not unique
    * No null values
12. `info`
    * Free-form English-language description of the athlete
    * String
    * Unique (excluding null values)
    * Contains null values


## Column definitions for `events.csv`

The event data is stored in [`events.csv`][evt]; one event per row, and six columns. There are 306 events across 50 disciplines in 28 sports; 161 for men, 136 for women, and 9 mixed sex.

1. `id`
    * Event id
    * Integer between 1 and 1,000,000
    * Unique
    * No null values
2. `sport`
    * The sport in which the event is categorised competes, as defined by the [IOC][ioc]
    * One of 28 lower-case string values (see `athletes.csv` column definitions for possible values)
    * Not unique
    * No null values
3. `discipline`
    * The event's sport sub-category; when a sport is not sub-categorised (e.g. football) simply a duplicate of column 2)
    * String up to 21 characters in length
    * Not unique
    * No null values
4. `name`
    * Name of the event
    * String up to 35 characters in length
    * Not unique
    * No null values
5. `sex`
    * Sex of the athletes competing in the event
    * One of two lower-case string values:
        * `male`
        * `female`
    * Not unique
    * No null values
6. `venues`
    * Names of the venues at which the event occurs; comma-separated list when an event occurs at more than one venue
    * String up to 112 characters in length
    * Not unique
    * No null values


[rio]: https://www.rio2016.com/
[blg]: https://flother.is/2017/olympic-games-data/
[ath]: https://raw.githubusercontent.com/flother/rio2016/master/athletes.csv
[evt]: https://raw.githubusercontent.com/flother/rio2016/master/events.csv
[tcc]: https://en.wikipedia.org/wiki/List_of_IOC_country_codes
[rot]: https://en.wikipedia.org/wiki/Refugee_Olympic_Team_at_the_2016_Summer_Olympics
[koc]: https://www.olympic.org/news/suspension-of-the-kuwait-olympic-committee
[ioc]: https://www.olympic.org/the-ioc
