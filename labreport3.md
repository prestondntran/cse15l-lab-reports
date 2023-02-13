# Lab Report 3: Researching the "grep" Command

## Command-Line Option 1: grep -c

**Example 1A**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/non-fiction/OUP/Fletcher
prestontran@Prestons-MacBook-Pro Fletcher % grep -c "Constitution" ch1.txt
14
```
The `grep -c` command returns the number of lines in `ch1.txt` that contain the string
`"Constitution"`. This can be useful in determining the relevance of a file in searching
for a specific topic: in this case, `ch1.txt` is found to be relevant to the topic of
the Constitution because there are 14 lines in the file that contain `"Constitution"`.

**Example 1B**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/travel_guides
prestontran@Prestons-MacBook-Pro travel_guides % find berlitz1 > berlitz1.txt
prestontran@Prestons-MacBook-Pro travel_guides % grep -c "LosAngeles" berlitz1.txt
4
```
In this example, a file called `berlitz1.txt` contains all the file names in the folder
`berlitz1`; the `grep -c` command returns the number of file names in `berlitz1.txt`
that contain the string `"LosAngeles"`. Using this command can help the user determine
the relevance of a directory in searching for a specific topic: in this instance, 
`berlitz1` is found to have files related to the topic of Los Angeles because there are 
4 files in the directory that have `"LosAngeles"` in the file names.

Source: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

## Command-Line Option 2: grep -i

**Example 2A**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/travel_guides/berlitz1
prestontran@Prestons-MacBook-Pro berlitz1 % grep -i "merchants" HistoryJapan.txt
        demands of the Tokugawa court. Merchants thronged to the large cities
        Merchants played an active role in creating the urban
        “accomplished person” — with a beauty and refinement that the merchants
        and a rigorous clamp-down on the merchants’ high life. There was no
```
The `grep -i` command returns all of the lines in `HistoryJapan.txt` that contain the
word merchants, regardless of lowercase or uppercase. This can be helpful in finding 
lines that contain the search word but have the word capitalized, as shown above in the
first two lines of the output.

**Example 2B**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/travel_guides       
prestontran@Prestons-MacBook-Pro travel_guides % find berlitz2 > berlitz2.txt
prestontran@Prestons-MacBook-Pro travel_guides % grep -i "History" berlitz2.txt
berlitz2/Portugal-History.txt
berlitz2/Costa-History.txt
berlitz2/Barcelona-History.txt
berlitz2/Berlin-History.txt
berlitz2/Bali-History.txt
berlitz2/Athens-History.txt
berlitz2/California-History.txt
berlitz2/Vallarta-History.txt
berlitz2/Cancun-History.txt
berlitz2/CostaBlanca-History.txt
berlitz2/NewOrleans-History.txt
berlitz2/PuertoRico-History.txt
berlitz2/Nepal-History.txt
berlitz2/China-History.txt
berlitz2/Canada-History.txt
berlitz2/Crete-History.txt
berlitz2/Amsterdam-History.txt
berlitz2/Beijing-History.txt
berlitz2/Bermuda-history.txt <History is not capitalized>
berlitz2/CanaryIslands-History.txt
berlitz2/Algarve-History.txt
berlitz2/Poland-History.txt
berlitz2/Budapest-History.txt
berlitz2/Cuba-History.txt
berlitz2/Bahamas-History.txt
```
In this example, a file called `berlitz2.txt` contains all the file names in the folder
`berlitz2`; the `grep -i` command finds all the file names in `berlitz2.txt` that
contain the word history. Using this command allows the user to find files whose names
contain the search word but aren't capitalized like the names of other files (or vice 
versa), such as the `Bermuda-history.txt` file shown above.

Source: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

## Command-Line Option 3: grep -n

**Example 3A**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/travel_guides/berlitz1
prestontran@Prestons-MacBook-Pro berlitz1 % grep -n "Vatican" WhereToItaly.txt
146:        imperial ruins; Catholic Rome of Vatican City and countless churches;
160:        the Vatican’s formidable complex, and come to know one age at a
229:        fleeing the malarial swamps of the Vatican down by the Tiber, housed
233:        city and the Vatican.
442:        The Vatican
445:        inspired by the splendors of Vatican City. At their best, the popes and
449:        to the Vatican is an object lesson for faithful and sceptic alike.
451:        Middle Ages was surrounded by a malarial swamp, the Vatican has been a
455:        the Vatican Museums on separate days to avoid fatigue and visual
468:        of their enemies below. Linked to the Vatican by a thick-walled
531:        Vatican Museums are made up of eight museums, five galleries, the
599:        Amid all the Vatican’s treasures, the 15 rooms of the
600:        Picture Gallery (Pinacoteca Vaticana), in a separate wing of the
606:        The neighborhood south of the Vatican, Trastevere,
1292:        have picked up a few tips for his future commission of the Vatican’s
3015:        his School of Athens fresco in the Vatican.
3600:        Soldiers for his Vatican fresco of St. Peter’s Crucifixion. The Titian
```
The `grep -n` command returns all of the lines in `WhereToItaly.txt` that contain the
string `"Vatican"` as well as the line numbers that they are located. This can be useful 
in finding the location of info on specific topics in large articles, such as where the
user can find info related to the Vatican City in the file `WhereToItaly.txt`.

**Example 3B**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/travel_guides
prestontran@Prestons-MacBook-Pro travel_guides % find berlitz2 > berlitz2.txt
prestontran@Prestons-MacBook-Pro travel_guides % grep -n "Budapest" berlitz2.txt
24:berlitz2/Budapest-WhereoGo.txt
32:berlitz2/Budapest-WhatToDo.txt
69:berlitz2/Budapest-History.txt
```
In this example, a file called `berlitz2.txt` contains all the file names in the folder
`berlitz2`; the `grep -n` command finds all the file names in `berlitz2.txt` that
contain the string `"Budapest"` and the line numbers that they are located. Using this
command can help the user to search large folders to find the location of files related 
to specific topics, such as files that are about Budapest.

Source: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

## Command-Line Option 4: grep -A n

**Example 4A**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/travel_guides/berlitz1
prestontran@Prestons-MacBook-Pro berlitz1 % grep -A 5 "Bingo" WhatToLasVegas.txt
        Bingo
        Nearly everyone knows the game of bingo, the mini-lottery
        in which players try to line up a horizontal or vertical row of
        randomly drawn numbers. The numbers are drawn until someone wins, and
        some veterans get up to 10 cards playing at once. No lessons are
        required.
```
The `grep -A n` command returns the line in `WhatToLasVegas.txt` that contains the string
`"Bingo"` as well as n lines after this line (in this case, five lines). This can be helpful 
in directly obtaining info on specific topics, such as learning more about Bingo by reading
its subsequent lines.

**Example 4B**
```
prestontran@Prestons-MacBook-Pro docsearch % cd written_2/travel_guides/berlitz1
prestontran@Prestons-MacBook-Pro berlitz1 % grep -A 3 "Batu Caves" WhereToMalaysia.txt
        pilgrimage to the Batu Caves (see page 53) commences.
        North and east of the historic center is KL’s “Golden
        Triangle,” which is a newer office, entertainment, and shopping
        district. Nearby are two of the tallest landmarks in the city. Visitors
--
        Batu Caves
        The giant Batu Caves are a popular excursion 45 minutes’
        drive north of town just off the Ipoh Road. Set in limestone cliffs
        hidden in the jungle, they were “discovered” in 1878 by a group of
        explorers, including the American naturalist William Hornaday. The
--
        from the Batu Caves is Templer Park, which offers the sights of a
        Malaysian rainforest for those with little time to venture into the
        major national parks and forested areas. Britain’s last High
        Commissioner, Sir Gerald Templer, conceived the park as a “vast jungle
```
In this example, the `grep -A n` command finds all the lines in `WhereToMalaysia.txt` that
contain the string `"Batu Caves"` as well as n lines after each instance (in this case, 3 lines). 
Using this command allows the user to determine whether lines in the output are relevant to their
search: in this case, only the second group of lines is relevant to the search of `"Batu Caves"`
because the subsequent lines discuss the caves, unlike the other two groups of lines.

Source: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
