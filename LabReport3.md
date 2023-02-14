# Lab Report 3

## Set up
For context, I first used find on the directory written_2 to save all of its contents to a file find-results.txt. This was so that I could use grep on find-results.txt since grep, by default, only searches the content of files, it cannot search the contents of a directory itself. 
![Image](written_2.png)

## Grep command's command line options
Here's what happens when I try to find the pattern "Bahamas" with the regular grep command
![Image](regularGrep.png)
In this example, grep searched the files for a specified pattern ("Bahamas") and outputs all lines that contain that pattern.
### Grep -c
With grep -c, grep will only print a count of the number of lines that contain the pattern, rather than the actual lines themselves.
Here is grep -c with the same pattern searched for previously ("Bahamas")
```
grep -c "Bahamas" find-results.txt
4
```
As we saw in the regular grep command call, we got 4 lines containing Bahamas listed out. With grep -c, we're only returned the number of lines containing the pattern. 

Here is an example of grep -c with word that appears more frequently in written_2
```
grep -c "fire" find-results.txt
9
```
I chose a random word that I believed would show more frequently, and it happened to appear in 9 lines throughout written_2. This example shows how useful it could be to use grep -c because if you have grep a pattern that occurs frequently throughout the file, then sometimes you don't want grep to list out each line that contains the pattern, but rather the count of number of lines that contain the pattern. For this command, I consulted chatGPT for help on how to use it and how it worked. 

### Grep -n
```
grep -n "Bahamas" find-results.txt
171:written_2/travel_guides/berlitz2/Bahamas-History.txt
172:written_2/travel_guides/berlitz2/Bahamas-Intro.txt
173:written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
174:written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```
Here is an example of the use of grep -n, which prints the line number of each match in addition to the actual line containing the pattern. 

```
grep -n Bahamas-History find-results.txt
171:written_2/travel_guides/berlitz2/Bahamas-History.txt
```

Here is a prime example of why grep -n can be useful. You want to find a specific pattern in a file/code and where it is. This could be useful when debugging for example, where you can grep -n and find what line and where you have bugs in your code. For this command, I also consulted chatGPT for help on how to use it and how it worked. 

### Grep -E
grep -E enables "extended regulr expressions" 
ChatGPT:"Extended regular expressions provide additional functionality compared to basic regular expressions, such as the ability to use square brackets to match a range of characters, and the ability to use the + and ? operators to match one or more or zero or one occurrences of a pattern, respectively."

```
grep -E "Bahamas|Portugal" find-results.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Portugal-History.txt
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
```
In the command above, I separated two patterns, Bahamas and Portugal, and -e allowed grep to search for files containing either of the two patterns. 
This shows how grep -E  can be useful to search for two patterns at once. 

```
grep -E "Bahamas[-]" find-results.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```

With the command above, I was able to use grep -E to find all lines containing the word Bahamas followed with -, denoted within the square brackets. This command allows grep to look for the specified word with the characters within the brackets following it. The square brackets are used to match a range of characters. I used chatGPT again to help me with this grep -E command.

### Grep -r
The grep -r option is used to search for a pattern recursively in a directory tree. When this option is used, grep will search for the pattern in all files in the specified directory, as well as in all subdirectories and their files, and so on.

```
grep -r "revolutionibus" written_2
written_2/travel_guides/berlitz2/Poland-History.txt:Polish nobles saw their political might expanded during the beginning of the Renaissance with the king’s “rule of the nobility,” which granted exclusive right to enact legislation to nobles in the parliament of Sejm. The 1500s were a time of prosperity, power, and cultural and scientific achievement for the Polish-Lithuanian Commonwealth. In 1543 Nicholas Copernicus, born in Toru´n and a graduate of the Jagiellonian University in Kraków, published his groundbreaking and astronomy-altering treatise, De **revolutionibus** orbium Coeliestium, which positioned the sun and not the earth as the center of the universe. Although the Reformation and Lutherism had an impact on Poland, the country largely avoided the devastating religious wars that raged elsewhere in Europe. 
```

With the -r option, grep will search for the pattern "revolutionibus" in all files under the directory written_2, including all subdirectories and their files. The output will show the file names and the line numbers where the pattern was found, along with the matching line of text. 

```
grep -r "congregation" written_2/travel_guides
written_2/travel_guides/berlitz1/HistoryJamaica.txt:        their congregations still as strong today as in the early 1800s.
written_2/travel_guides/berlitz1/IntroGreek.txt:        Women have traditionally formed the majority of the congregation,
written_2/travel_guides/berlitz1/WhereToIndia.txt:        congregational “Friday Mosque”), is the largest mosque in India. The
written_2/travel_guides/berlitz1/WhereToMadrid.txt:        congregation. Curiously, Christian tombstones are found in the floor;
written_2/travel_guides/berlitz2/Athens-Intro.txt:The Orthodox Church — for so long the one thing that united the Hellenic Diaspora — still has a strong influence on the population. Everyone from suited businessmen to young soldiers on national service make a regular visit to Athens Cathedral or a small local church to light a candle. People stop in on the way home from work or in their lunch breaks; it’s such a normal part of everyday life here. The Greek language also unifies the congregation with the clergy and Greeks around the world, though its use gives the capital a decidedly exotic air as visitors struggle to make sense of these “foreign” letters. There’s also a sense of patriotism and national pride here even among the young — perhaps brought about by political upheavals in the late 20th century. Since Greek democracy was restored in 1975, after the military dictatorship, it is as though the population relish their country all the more.
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt:The site of the monastery is spectacular, tucked into folds of rock high above the plain. On the eve of the saint’s day, 27 April, the monks hold an all-night vigil attended by crowds of people. La Moreneta looks down from a gold-and-glass case above and to the right of the altar in the basilica, but the faithful can touch or kiss her right hand through an opening. At 1pm and 7pm (except in July), the choir boys of the Escolanía, one of the world’s oldest music schools, founded in the 13th century, fill the basilica with their angelic voices. The congregation joins in at the end of the service to sing Montserrat’s hymn, the Virolai, an expression of faith fused with a nationalist fervor.
written_2/travel_guides/berlitz2/Bermuda-history.txt:Progress was swift during the first few years of the colony’s existence. In 1619 the congregation of St. Peter’s Church moved into a permanent building, and Bermuda’s parliament met in an enclosure still visible amid the pews. But it was soon decided to separate the secular from the religious, and a new government building went up. State House, Bermuda’s first stone structure, is still standing today in St. George’s.
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:Continue northward along Tremont Street to the squat, granite King’s Chapel (summer Monday, Thursday– Saturday 9am–4pm; winter Saturday only 9am–4pm). The first Anglican place of worship in Boston, it stands on land taken by Governor Andros from the burial ground next door: The Puritans refused to sell any land that would be used to benefit a denomination that had persecuted them. Royal officials and wealthy merchants worshiped here until the Revolution caused a split in the congregation and placed the church in jeopardy. After the Revolution it became the first Unitarian church in the nation, even while it retained much of the ritual and musical tradition of the earlier church (frequent lunchtime and other concerts are given). The magnificent interior, one of the finest examples of Georgian church architecture in North America, has lavishly upholstered pews — especially the governor’s — gilt crown and miters on the organ case, the oldest pulpit in the nation, and a bell cast by Paul Revere that was tolled at his death.
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:Except for quotations on the walls from the New Testament and Christian Science founder, Mary Baker Eddy, there’s no decoration. Some stained glass windows are found in the older church, which also contains founder Mary Baker Eddy’s chair. She only addressed the congregation twice, as she wished to avoid any personal idolatry. A guided tour is highly recommended (you can only visit the original church by joining a tour).
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Perhaps one of the most beautiful and unusual buildings in Charlotte Amalie is the St. Thomas Synagogue, on Crystal Gade. This is the oldest synagogue building in continual use under the American flag. The Jewish congregation has always been strong here, from the very earliest days of Danish settlement in 1655. When the all-consuming fire of 1831 broke out, 64 families were worshipping in the small synagogue. Only one scroll could be saved before the flames destroyed the building. The present structure was built on the same spot and opened in 1833. The synagogue has sand on the floor, symbolic of the Jewish flight from Egypt.
```
With the -r option, grep will search for the pattern "congregations" in all files under the directory written_2/travel_guides, including all subdirectories and their files. The output will show the file names and the line numbers where the pattern was found, along with the matching line of text. grep -r can be useful when you need to search for a pattern across a large number of files in multiple directories, as it can save you time and effort compared to searching for the pattern in each file separately. I used chatGPT for help with the grep -r command. 




