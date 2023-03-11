# LAB REPORT 5 #

## GREP COMMAND ##

### Case Insensitive Search

```grep -i [text] [file-path]``` will search for a given piece of text case insensitively. This is useful in case you are searching for a specific word but don't know if it is capitalized or not, or if it might be found at the beginning of a sentence.

Searching for case insensitive "swim" within HandRHawaii.txt

```
$ grep -i "swim" written_2/travel_guides/berlitz1/HandRHawaii.txt 
        palms, and swimming pools. There are dozens of shops, a spa, and a
        beach, swimming pool, and lagoon with resident turtles and dolphins.
        with exotic birds, waterfalls, garden atriums, and sculpted swimming
        away is one of the island’s best snorkeling and swimming beaches. 311
        complex, and five swimming pools facing the ocean. 243 rooms.
        rooms, the Hilton is best known for its swim-with-the-dolphins program.
        There’s also a 1-acre swimming pool with water slides and a vast array
        cove and reef where the freed turtles await swimmers and snorkelers.
        full-service resort fronts a tremendous swimming and snorkeling beach
        the best hotel pools and swimming beaches in Hawaii. 419 rooms.
        buildings facing a lava rock shoreline. Swimming pools, spa, tennis,
        apartments, a swimming poo1, tennis courts, and a golf course. Walk to
```

Searching for case insensitive "casino" in WhatToLasVegas.txt
```
$ grep -i "casino" written_2/travel_guides/berlitz1/WhatToLasVegas.txt 
        the two overlap, often to the point of indistinctness. Casinos and
        Strip, where nearly twenty major casinos in excess of 100,000 sq ft
        furious, with generally inflexible house rules. Downtown casinos are a
        the casino.
        casinos offer a variety of video game slot machines. Try Bally’s for
        sections of the casino. Gambling lessons are highly recommended for
        that of any other casino game — but it’s an inexpensive way to pass the
        the play at table games in many casinos. Though all modern slot
        long as the bottom line shined, casino operators, especially those in
        accounting procedures, every sector of a hotel-casino had to show
        Girls impersonators still have Ginger. Stratosphere Hotel and Casino,
        Casino, 3570 Las Vegas Boulevard South; Tel. (702) 731-7110. Multiple
        Hotel and Casino, 3600 Las Vegas Boulevard South; Tel. (702) 693-7111.
        entertainment. Mirage Hotel and Casino, 7900 Las Vegas Boulevard South;
        for all ages. MGM Grand Hotel and Casino, 3799 Las Vegas Boulevard
        theater named for “Mr. Vegas” himself. Stardust Resort and Casino, 3000
        powerful. Luxor Hotel and Casino, 3900 Las Vegas Boulevard South; Tel.
        adults only. Bally’s Hotel and Casino, 3645 Las Vegas Boulevard South;
        for families. Excalibur Hotel and Casino, 3850 Las Vegas Boulevard
        Tina Turner. Imperial Palace Hotel and Casino, 3535 Las Vegas Boulevard
        dancers. Monte Carlo Hotel and Casino, 3770 Las Vegas Boulevard South;
        and Casino, 3790 Las Vegas Boulevard South; Tel. (702) 740-6969. Shows
        1500-seat showroom. Mirage Hotel and Casino, 3400 Las Vegas Boulevard
        Casino, 2901 Las Vegas Boulevard South; Tel. (702) 734-5110. Shows 7:30
        showgirls is what the myth was based on. Tropicana Resort and Casino,
        Casino, the mall houses interesting specialty stores in addition to
        are a surprising number of kid-friendly activities. Most casinos have
        friendly hotel-casino, and in recent years has tried to up the ante
        tag arena. It’s located behind the venerable hotel-casino, which itself
        Want to get the kids away from the casinos? Try the
```

### Count Number of Search Matches

```grep -c [text] [file-path]``` will search for a given piece of text within a file and return the number of times that the desired text is found. This is useful in case you want to briefly search if a word is mentioned in a file or how often it shows up.

Finding how many times "food" is found in WhatToItaly.txt
```
$ grep -c "food" written_2/travel_guides/berlitz1/WhatToItaly.txt 
1
```

Finding how many times "wine" is found in IntroFrance.txt
```
$ grep -c "wine" written_2/travel_guides/berlitz1/IntroFrance.txt 
3
```

### Find Files with Search Matches

```grep -l [text] [file-paths]``` will search for a given piece of text within files and return the names of the files that contain the desired text. This is incredibly useful in finding relevant files to a certain word or topic, and can be applied to entire directories.

Finding the files in the berlitz1 directory containing "party"
```
$ grep -l "party" written_2/travel_guides/berlitz1/*
written_2/travel_guides/berlitz1/HandRIsrael.txt
written_2/travel_guides/berlitz1/HistoryEgypt.txt
written_2/travel_guides/berlitz1/HistoryFWI.txt
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/HistoryIbiza.txt
written_2/travel_guides/berlitz1/HistoryIndia.txt
written_2/travel_guides/berlitz1/HistoryIstanbul.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/HistoryJamaica.txt
written_2/travel_guides/berlitz1/HistoryJapan.txt
written_2/travel_guides/berlitz1/HistoryLasVegas.txt
written_2/travel_guides/berlitz1/HistoryMadrid.txt
written_2/travel_guides/berlitz1/HistoryMalaysia.txt
written_2/travel_guides/berlitz1/IntroEdinburgh.txt
written_2/travel_guides/berlitz1/IntroIndia.txt
written_2/travel_guides/berlitz1/IntroMadrid.txt
written_2/travel_guides/berlitz1/IntroMallorca.txt
written_2/travel_guides/berlitz1/WhatToEgypt.txt
written_2/travel_guides/berlitz1/WhatToGreek.txt
written_2/travel_guides/berlitz1/WhatToHongKong.txt
written_2/travel_guides/berlitz1/WhatToMadeira.txt
written_2/travel_guides/berlitz1/WhereToFWI.txt
written_2/travel_guides/berlitz1/WhereToGreek.txt
written_2/travel_guides/berlitz1/WhereToJapan.txt
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
```

Finding the files in the berlitz1 directory containing "progressive"
```
$ grep -l "progressive" written_2/travel_guides/berlitz1/*
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/HistoryIndia.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/HistoryLasVegas.txt
written_2/travel_guides/berlitz1/IntroItaly.txt
written_2/travel_guides/berlitz1/WhatToItaly.txt
written_2/travel_guides/berlitz1/WhatToMallorca.txt
written_2/travel_guides/berlitz1/WhereToJapan.txt
```

### Finding Whole Words
```grep -w [text] [file-path]``` searches for the given text as a whole word, meaning no instances of the text as a substring will be returned. This is helpful if you are searching for one word in specific, and don't want to look at unrelated instances. This might also be useful if you are searching for a specific action/verb and do not want results of other tenses (for example, run vs running).

Searching for "rule" in HistoryJapan.txt (should have no instances of "ruler," "ruled," or otherwise)
```
$ grep -w "rule" written_2/travel_guides/berlitz1/HistoryJapan.txt 
        food resources. This set the pattern of hierarchic rule that was to
        Fujiwara clan, which was to rule Japanese affairs for hundreds of years
        During its subsequent two and a half centuries of rule from

```

Searching for "rule" in HistoryJapan.txt without ```-w```
```
$ grep "rule" written_2/travel_guides/berlitz1/HistoryJapan.txt 
        food resources. This set the pattern of hierarchic rule that was to
        the most part) only nominally ruled by the emperor. De facto power was
        Fujiwara clan, which was to rule Japanese affairs for hundreds of years
        Japan’s austere, ruthless, but statesmanlike new ruler,
        national rulers to take the title of sei-i tai-shogun
        During its subsequent two and a half centuries of rule from
        enforce the (short-lived) new rules.
        quickly followed. And to show just how fast Japan’s new rulers were
        experienced under their former colonial rulers.
```

Searching for "Christian" in HistoryMadrid.txt (should have no instances of "Christians," "Christianized," etc.)
```
$ grep -w "Christian" written_2/travel_guides/berlitz1/HistoryMadrid.txt 
        Christian reconquest. Over centuries of struggle, the defending Moorish
        After several unsuccessful skirmishes, the Christian forces
```

Searching for "Christian" in HistoryMadrid.txt without ```-w```
```
$ grep "Christian" written_2/travel_guides/berlitz1/HistoryMadrid.txt 
        Christian reconquest. Over centuries of struggle, the defending Moorish
        After several unsuccessful skirmishes, the Christian forces
        overrun by the Moors, but the Christianized fortress held. The Moors
```

*All commands found on [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)*
