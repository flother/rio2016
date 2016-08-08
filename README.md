This dataset includes the official statistics on all 11,482 athletes (6,299 men and 5,183 women) at the 2016 Olympic Games in Rio de Janeiro. The data is taken from the [Rio 2016 website] [rio]. Flaws in the source data are reflected here.

* [Download the latest athlete data as a CSV] [csv]

## Column definitions

The athlete data is stored in [`athletes.csv`] [csv]; one athlete per row, and eleven columns. Empty cells are null values.

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
    * One of the [IOC] [ioc]'s 206 [three-letter country codes] [tcc], or `ROT` for members of the [Refugee Olympic Team] [rot]. Kuwaiti athletes' nationality is given as `IOA` due to the [suspension of the Kuwait Olympic Committee] [koc]
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
    * Contains a single null value, for Russia's [Pavel Sozykin] [psr]
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
    * The sport in which the athlete competes, as defined by the [IOC] [ioc]
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


[rio]: https://www.rio2016.com/
[csv]: http://rawgit.com/flother/rio2016/master/athletes.csv
[tcc]: https://en.wikipedia.org/wiki/List_of_IOC_country_codes
[rot]: https://en.wikipedia.org/wiki/Refugee_Olympic_Team_at_the_2016_Summer_Olympics
[koc]: https://www.olympic.org/news/suspension-of-the-kuwait-olympic-committee
[psr]: https://www.rio2016.com/en/athlete/pavel-sozykin-rus
[ioc]: https://www.olympic.org/the-ioc

