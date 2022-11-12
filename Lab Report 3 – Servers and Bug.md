**Lab Report 3 – Servers and Bugs**

For this report, I am going to search about **grep** command. 

1. grep -c <br/>
grep -c found specific word in a document and count the specific words in a document. <br/> This is how we use grep -c.

This is the one way to use grep -c <br/>
grep -c 
(specificword) (path of the document)<br/>

Lets learn more about **grep -c** command by using examples!<br/>

[First Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -c government technical/911report/chapter-13.1.txt
39
```
I used grep -c to find word "government" in the chapter-13.1 txt. It seems word "government" repeated 39 times in the chapter -13.1.txt.

[Second Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -c California technical/911report/chapter-7.txt
13
```
This time i wanted to find word "California". In the chapter-7.txt, word "California" repeated 13 times. 
[Third Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -c Bin  technical/911report/chapter-2.txt
157
```
Also, in chapter-2.txt, word "Bin" repeated 157 times.

By using grep -c, we can easily count the specific word, so it will be useful when we want to count word in a document. 


2. grep -w

grep -w found a specific word and also,print the sentence that contains the specic word. <br/>
Different from grep -c, we need to put a specific word in "".

Lets learn more about **grep -w** command by using examples!<br/>


[First Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -w "chemical" technical/plos/journal.pbio.0020035.txt
        medicines for treating infectious disease. The most important chemical class of these
        While many different chemical classes are represented amongst actinomycete antibiotics,
        all those mentioned above. This chemical family is made up of the polyketides. They are
        ‘tailoring’ enzymes can then add sugars or other chemical groups to it at many alternative
        positions, enabled by the pattern of chemical reactivity built into the polyketide by the
        chemical and biochemical experiments to begin to crack this ‘polyketide code’. The first
```
<br/> I used grep -w to find word "chemical" and print the sentence that contains the word "chemical". 

[Second Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -w "cancer" technical/plos/pmed.0010066.txt
        survival in breast cancer [2]. The total nodal tumor burden (number of affected nodes and
        detection of cancer in nonenlarged (occult) nodes is often quite low by positron-emission
        nodal metastases (< 5 mm) are often missed by PET imaging in patients with breast cancer
        in prostate cancer [17]. These nanoparticles serve as probes for lymphatic anatomy and
        Despite the advances of LMRI for cancer staging, image analysis has been challenging and
          retroperitoneum. In patients with breast cancer (
          of a 45-y-old patient with colorectal cancer undergoing semiautomated nodal staging. In
          cancer primary with bilateral nodal metastases. Note the high spatial resolution allowing
        the likelihood of nodal metastases in vivo. These results are highly relevant in cancer
        presence mandates the need for more extensive and systemic therapy. Nodal cancer staging
        cancer. Accurate staging represents the cornerstone for triaging patients to either
        surgical fields, this information may influence surgical approaches. In colorectal cancer,
```
<br/> This time the terminal printed out the sentence that contains word "cancer". 

[Third Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -w "protein" technical/plos/journal.pbio.0020047.txt
        Inside eukaryotic cells there is a massive protein complex called the proteasome whose
        proteins are first “labeled” by the addition of several copies of a small protein tag
        ubiquitination of proteins is regulated through precise selection of protein substrates by
        amino group on the target protein via an amide bond (Figure 1).
        Interestingly, ubiquitination is a reversible process. Even when a protein has been
        for proteolysis of ubiquitin–protein conjugates, but not of unstructured polypeptides
        protein-eating machine hints at the exquisite controls that must rgulate its function.
        in regulated protein degradation. Both are made up of eight homologous protein subunits
        doubt uncover additional mechanisms whereby ubiquitin-mediated protein degradation is
        linking deubiquitination with protein degradation. Notably, Rpn11 shares close homology
        + /JAMM protein from an archaebacterium (Ambroggio et al. 2003; Tran et
        nucleophile. Overall, this protein certainly has properties consistent with a
        core proteolytic subunits process the target protein itself (Figure 1). However, this still
```

Also in example 3, we can find the sentence that contains word "protein". 

Using grep -w is useful when we try to find out the brief information about the word in the document. For example, if we want to know the information about protein in the 0020047.txt, we could use grep -w and by reading the sentence we can briefly know what the protein in the document. 

3. grep -i
grep -i find and print the sentence that contains the specific word that is after grep -i. <br/>
The difference between grep -w and grep - is that, in grep -i the upper case and lower case of the word is igonred. Also, I observed that grep - i is printing more one or two more sentence that comes after or before the sentence that contains the specific word. 

[First Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -i "World" technical/911report/*.txt                 
technical/911report/chapter-1.txt:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
technical/911report/chapter-1.txt:    At 8:46:40, American 11 crashed into the North Tower of the World Trade Center in New York City.
technical/911report/chapter-1.txt:    The call ended abruptly. Lee Hanson had heard a woman scream just before it cut off. He turned on a television, and in her home so did Louise Sweeney. Both then saw the second aircraft hit the World Trade Center.
technical/911report/chapter-1.txt:    At 9:03:11, United Airlines Flight 175 struck the South Tower of the World Trade Center.
technical/911report/chapter-1.txt:    At 9:00, American Airlines Executive Vice President Gerard Arpey learned that communications had been lost with American 77. This was now the second American aircraft in trouble. He ordered all American Airlines flights in the Northeast that had not taken off to remain on the ground. Shortly before 9:10, suspecting that American 77 had been hijacked, American headquarters concluded that the second aircraft to hit the World Trade Center might have been Flight 77. After learning that United Airlines was missing a plane, American Airlines headquarters extended the ground stop nationwide.
technical/911report/chapter-1.txt:    As United 93 left Newark, the flight's crew members were unaware of the hijacking of American 11. Around 9:00, the FAA, American, and United were facing the staggering realization of apparent multiple hijackings. At 9:03, they would see another aircraft strike the World Trade Center. Crisis managers at the FAA and the airlines did not yet act to warn other aircraft.
technical/911report/chapter-1.txt:    No one at the FAA or the airlines that day had ever dealt with multiple hijackings. Such a plot had not been carried out anywhere in the world in more than 30 years, and never in the United States. As news of the hijackings filtered through the FAA and the airlines, it does not seem to have occurred to their leadership that they needed to alert other aircraft in the air that they too might be at risk.
technical/911report/chapter-1.txt:    The airlines bore responsibility, too. They were facing an escalating number of conflicting and, for the most part, erroneous reports about other flights, as well as a continuing lack of vital information from the FAA about the hijacked flights. We found no evidence, however, that American Airlines sent any cockpit warnings to its aircraft on 9/11. United's first decisive action to notify its airborne aircraft to take defensive action did not come until 9:19, when a United flight dispatcher, Ed Ballinger, took the initiative to begin transmitting warnings to his 16 transcontinental flights: "Beware any cockpit intrusion- Two a/c [aircraft] hit World Trade Center." One of the flights that received the warning was United 93. Because Ballinger was still responsible for his other flights as well as Flight 175, his warning message was not transmitted to Flight 93 until 9:23.
technical/911report/chapter-1.txt:    Shortly thereafter, the passengers and flight crew began a series of calls from GTE airphones and cellular phones. These calls between family, friends, and colleagues took place until the end of the flight and provided those on the ground with firsthand accounts. They enabled the passengers to gain critical information, including the news that two aircraft had slammed into the World Trade Center.
technical/911report/chapter-1.txt:    At least two callers from the flight reported that the hijackers knew that passengers were making calls but did not seem to care. It is quite possible Jarrah knew of the success of the assault on the World Trade Center. He could have learned of this from messages being sent by United Airlines to the cockpits of its transcontinental flights, including Flight 93, warning of cockpit intrusion and telling of the New York attacks. But even without them, he would certainly have understood that the attacks on the World Trade Center would already have unfolded, given Flight 93's tardy departure from Newark. If Jarrah did know that the passengers were making calls, it might not have occurred to him that they were certain to learn what had happened in New York, thereby defeating his attempts at deception.
technical/911report/chapter-1.txt:    During at least five of the passengers' phone calls, information was shared about the attacks that had occurred earlier that morning at the World Trade Center. Five calls described the intent of passengers and surviving crew members to revolt against the hijackers. According to one call, they voted on whether to rush the terrorists in an attempt to retake the plane. They decided, and acted.
technical/911report/chapter-1.txt:    NEADS: Is this real-world or exercise?
technical/911report/chapter-1.txt:    F-15 fighters were scrambled at 8:46 from Otis Air Force Base. But NEADS did not know where to send the alert fighter aircraft, and the officer directing the fighters pressed for more information:"I don't know where I'm scrambling these guys to. I need a direction, a destination." Because the hijackers had turned off the plane's transponder, NEADS personnel spent the next minutes searching their radar scopes for the primary radar return. American 11 struck the NorthTower at 8:46. Shortly after 8:50, while NEADS personnel were still trying to locate the flight, word reached them that a plane had hit the World Trade Center. 
technical/911report/chapter-1.txt:    Another commercial aircraft in the vicinity then radioed in with "reports over the radio of a commuter plane hitting the World Trade Center." The controller spent the next several minutes handing off the other flights on his scope to other controllers and moving aircraft out of the way of the unidentified aircraft (believed to be United 175) as it moved southwest and then turned northeast toward New York City.
technical/911report/chapter-1.txt:    Boston Center: It sounds like, we're talking to New York, that there's another one aimed at the World Trade Center.
technical/911report/chapter-1.txt:    By 9:08, the mission crew commander at NEADS learned of the second explosion at the World Trade Center and decided against holding the fighters in military airspace away from Manhattan:
technical/911report/chapter-1.txt:    By 9:25, FAA's Herndon Command Center and FAA headquarters knew two aircraft had crashed into the World Trade Center. They knew American 77 was lost. At least some FAA officials in Boston Center and the New England Region knew that a hijacker on board American 11 had said "we have some planes." Concerns over the safety of other aircraft began to mount. A manager at the Herndon Command Center asked FAA headquarters if they wanted to order a "nationwide ground stop." While this was being discussed by executives at FAA headquarters, the Command Center ordered one at 9:25.
technical/911report/chapter-1.txt:    The mention of a "third aircraft" was not a reference to American 77. There was confusion at that moment in the FAA. Two planes had struck the World Trade Center, and Boston Center had heard from FAA headquarters in Washington that American 11 was still airborne. We have been unable to identify the source of this mistaken FAA information.
technical/911report/chapter-1.txt:    Right after the Pentagon was hit, NEADS learned of another possible hijacked aircraft. It was an aircraft that in fact had not been hijacked at all. After the second World Trade Center crash, Boston Center managers recognized that both aircraft were transcontinental 767 jetliners that had departed Logan Airport. Remembering the "we have some planes" remark, Boston Center guessed that Delta 1989 might also be hijacked. Boston Center called NEADS at 9:41 and identified Delta 1989, a 767 jet that had left Logan Airport for Las Vegas, as a possible hijack. NEADS warned the FAA's Cleveland Center to watch Delta 1989. The Command Center and FAA headquarters watched it too. During the course of the morning, there were multiple erroneous reports of hijacked aircraft. The report of American 11 heading south was the first; Delta 1989 was the second.
technical/911report/chapter-1.txt:    In this same public testimony, NORAD officials stated that at 9:24, NEADS received notification of the hijacking of American 77. This statement was also incorrect. The notice NEADS received at 9:24 was that American 11 had not hit the World Trade Center and was heading for Washington, D.C.
technical/911report/chapter-1.txt:    When American 11 struck the World Trade Center at 8:46, no one in the White House or traveling with the President knew that it had been hijacked. While that information circulated within the FAA, we found no evidence that the hijacking was reported to any other agency in Washington before 8:46.
technical/911report/chapter-1.txt:    In Sarasota, Florida, the presidential motorcade was arriving at the Emma E. Booker Elementary School, where President Bush was to read to a class and talk about education. White House Chief of Staff Andrew Card told us he was standing with the President outside the classroom when Senior Advisor to the President Karl Rove first informed them that a small, twin-engine plane had crashed into the World Trade Center. The President's reaction was that the incident must have been caused by pilot error.
technical/911report/chapter-1.txt:    At 8:55, before entering the classroom, the President spoke to National Security Advisor Condoleezza Rice, who was at the White House. She recalled first telling the President it was a twin-engine aircraft-and then a commercial aircraft-that had struck the World Trade Center, adding "that's all we know right now, Mr. President."
technical/911report/chapter-1.txt:    At the White House, Vice President Dick Cheney had just sat down for a meeting when his assistant told him to turn on his television because a plane had struck the NorthTower of the World Trade Center. The Vice President was wondering "how the hell could a plane hit the World Trade Center" when he saw the second aircraft strike the South Tower.
technical/911report/chapter-1.txt:    When they learned a second plane had struck the World Trade Center, nearly everyone in the White House told us, they immediately knew it was not an accident. The Secret Service initiated a number of security enhancements around the White House complex. The officials who issued these orders did not know that there were additional hijacked aircraft, or that one such aircraft was en route to Washington. These measures were precautionary steps taken because of the strikes in New York.
technical/911report/chapter-1.txt:    Inside the NMCC, the deputy director for operations called for an allpurpose "significant event" conference. It began at 9:29, with a brief recap: two aircraft had struck the World Trade Center, there was a confirmed hijacking of American 11, and Otis fighters had been scrambled. The FAA was asked to provide an update, but the line was silent because the FAA had not been added to the call. A minute later, the deputy director stated that it had just been confirmed that American 11 was still airborne and heading toward D.C. He directed the transition to an air threat conference call. NORAD confirmed that American 11 was airborne and heading toward Washington, relaying the erroneous FAA information already mentioned. The call then ended, at about 9:34.
technical/911report/chapter-10.txt:                worldwide. Finally, he directed Treasury Secretary Paul O'Neill to craft a plan to
technical/911report/chapter-10.txt:                11 years, and was the only place in the world where the United States was engaged in
technical/911report/chapter-10.txt:                1993 attack on the World Trade Center. 73 The next day, Wolfowitz renewed the
technical/911report/chapter-10.txt:                on their contingency plans. Though he emphasized the worldwide nature of the
technical/911report/chapter-11.txt:                reimagine, as that past world, with its preoccupations and uncertainty, recedes and
technical/911report/chapter-11.txt:            The United States emerged into the post-Cold War world as the globe's preeminent
technical/911report/chapter-11.txt:                Yousef, who organized the 1993 bombing of the World Trade Center, and Mir Amal
technical/911report/chapter-11.txt:                such as sports arenas, and civil aviation generally. It warned that the 1993 World
technical/911report/chapter-11.txt:                They operate "outside traditional circles but have access to a worldwide network of
technical/911report/chapter-11.txt:                information that a group of Libyans hoped to crash a plane into the World Trade
technical/911report/chapter-11.txt:                to achieve in its energetic worldwide efforts to disrupt terrorist activities or use
technical/911report/chapter-11.txt:                part of a general regional or worldwide alert, they might have tracked him coming
technical/911report/chapter-12.txt:                Threat In the post-9/11 world, threats are defined more by the fault lines within
technical/911report/chapter-12.txt:                rather than international. That is the defining quality of world politics in the
technical/911report/chapter-12.txt:                world-against the U.S. military presence in the Middle East, policies perceived as
technical/911report/chapter-12.txt:            Because the Muslim world has fallen behind the West politically, economically, and
technical/911report/chapter-12.txt:                conditions in the Muslim world, conditions that spill over into expatriate Muslim
technical/911report/chapter-12.txt:                the Islamic world, inspired in part by al Qaeda, which has spawned terrorist groups
technical/911report/chapter-12.txt:                terror. America and its friends oppose a perversion of Islam, not the great world
technical/911report/chapter-12.txt:                military. The strategy must focus clearly on the Arab and Muslim world, in all its
technical/911report/chapter-12.txt:                terrorism? The goals seem unlimited: Defeat terrorism anywhere in the world. But
technical/911report/chapter-12.txt:                popularly described as being all over the world, adaptable, resilient, needing
technical/911report/chapter-12.txt:            The U.S.government, joined by other governments around the world, is working through
technical/911report/chapter-12.txt:                in the world. The intelligence community has prepared a world map that highlights
technical/911report/chapter-12.txt:                with the outside world. Large areas scattered around the world meet these
technical/911report/chapter-12.txt:            In the twentieth century, strategists focused on the world's great industrial
technical/911report/chapter-12.txt:                    strategy of "enlightened moderation." The Muslim world, he said, should shun
technical/911report/chapter-12.txt:                    seek to resolve disputes with justice and help better the Muslim world.
technical/911report/chapter-12.txt:                    following through; some of the other states around the world that have pledged
technical/911report/chapter-12.txt:            The Kingdom is one of the world's most religiously conservative societies, and its
technical/911report/chapter-12.txt:                works is an integral function of the governments in the Islamic world. It is so
technical/911report/chapter-12.txt:            Traditionally, throughout the Muslim world, there is no formal oversight mechanism
technical/911report/chapter-12.txt:                Welfare, charities and international relief agencies, such as the World Assembly of
technical/911report/chapter-12.txt:                the world, including in mosques and schools. Often these schools provide the only
technical/911report/chapter-12.txt:                the supply and price of oil in world markets, and in Saudi hopes that America could
technical/911report/chapter-12.txt:                Abdullah wants the Kingdom to join the World Trade Organization to accelerate
technical/911report/chapter-12.txt:                was highly critical of the Arab world's political, economic, and social failings and
technical/911report/chapter-12.txt:                    the outside world. It should include a shared interest in greater tolerance and
technical/911report/chapter-12.txt:            The United States is heavily engaged in the Muslim world and will be for many years
technical/911report/chapter-12.txt:                America in most of the Muslim world. Negative views of the U.S. among Muslims, which
technical/911report/chapter-12.txt:                    what it stands for. We should offer an example of moral leadership in the world,
technical/911report/chapter-12.txt:                    leaders in the Arab and Muslim world, a moderate consensus can be found.
technical/911report/chapter-12.txt:                popular commentary across the Arab and Muslim world. That does not mean U.S. choices
technical/911report/chapter-12.txt:                opportunity to the Arab and Muslim world. Neither Israel nor the new Iraq will be
technical/911report/chapter-12.txt:                safer if worldwide Islamist terrorism grows stronger.
technical/911report/chapter-12.txt:                a cave outcommunicate the world's leading communications society?" Deputy Secretary
technical/911report/chapter-12.txt:                    act aggressively to define itself in the Islamic world, the extremists will
technical/911report/chapter-12.txt:                        television and radio broadcasting to the Arab world, Iran, and Afghanistan.
technical/911report/chapter-12.txt:                    translate more of the world's knowledge into local languages and libraries to
technical/911report/chapter-12.txt:                    house such materials. Education about the outside world, or other cultures, is
technical/911report/chapter-12.txt:                    regions of the world.
technical/911report/chapter-12.txt:                future of the Arab and Muslim world. These new international efforts can create
technical/911report/chapter-12.txt:                    standards are generally accepted throughout the world as customary international
technical/911report/chapter-12.txt:                materialize if the world's most dangerous terrorists acquire the world's most
technical/911report/chapter-12.txt:                public portion of his February 2004 worldwide threat assessment to Congress,
technical/911report/chapter-12.txt:                Yousef parked in the garage of the World Trade Center in 1993. Such a bomb would
technical/911report/chapter-12.txt:                capture, interdiction, and prosecution of such smugglers by any state in the world
technical/911report/chapter-12.txt:                and thus virtually ensuring that little money is actually frozen. Worldwide asset
technical/911report/chapter-12.txt:                    governments could dramatically strengthen America and the world's collective
technical/911report/chapter-12.txt:                element at the World Trade Center, Pentagon, and Somerset County, Pennsylvania,
technical/911report/chapter-12.txt:                in the World Trade Center emergency demonstrated the need for these standards.
technical/911report/chapter-12.txt:                    world. It is ignored at a tremendous potential cost in lives, money, and
technical/911report/chapter-13.1.txt:                confronts a very different world today. Instead of facing a few very dangerous
technical/911report/chapter-13.1.txt:            The men and women of the World War II generation rose to the challenges of the 1940s
technical/911report/chapter-13.1.txt:                system designed generations ago for a world that no longer exists.
technical/911report/chapter-13.1.txt:                models of management needed to deal with the twenty-first-century world.
technical/911report/chapter-13.1.txt:                analogy is weak-the actual British Security Service is a relatively small worldwide
technical/911report/chapter-13.2.txt:                World Trade Center, Melody Homer, the wife of co-pilot Leroy Homer, had an ACARS
technical/911report/chapter-13.2.txt:                military's response to the real-world terrorist attack on 9/11. According to General
technical/911report/chapter-13.2.txt:                Eberhart, " it took about 30 seconds" to make the adjustment to the real-world
technical/911report/chapter-13.2.txt:                rate of descent, the radar target terminated at the World Trade Center.'" FAA
technical/911report/chapter-13.2.txt:                10:02:22. 2 The Foundation of the New Terrorism 1." Text of World Islamic Front's
technical/911report/chapter-13.2.txt:                world audience and signed by Usama Bin Ladin, Ayman al Zawahiri (emir of the
technical/911report/chapter-13.3.txt:                Arab dominance of the Muslim world. Moghul India, Safavid Persia, and, above all,
technical/911report/chapter-13.3.txt:                throughout the Arab world in the mid-twentieth century. In some countries, its
technical/911report/chapter-13.3.txt:                to America,'" Observer Worldview, Nov. 24, 2002 (trans., online at
technical/911report/chapter-13.3.txt:                http://observer.guardian.co.uk/worldview/story/0,11581,845725,00.html). The al Qaeda
technical/911report/chapter-13.3.txt:                Foundation (BIF) and World Association of Muslim Youth, 1991).
technical/911report/chapter-13.3.txt:                Holy War Inc.: Inside the Secret World of Osama bin Ladin (Touchstone, 2001), pp.
technical/911report/chapter-13.3.txt:                and KSM helped fund Yousef 's attempt to blow up the World Trade Center in 1993.
technical/911report/chapter-13.3.txt:                to Yousef and the 1993 World Trade Center attack, while Wali Khan was convicted
technical/911report/chapter-13.3.txt:                events from 1993 bombing of World Trade Center through 9/11 (citing cables from Apr.
technical/911report/chapter-13.3.txt:            88." World Islamic Front's Statement Urging Jihad," Al Quds al Arabi, Feb. 23, 1998;
technical/911report/chapter-13.3.txt:                Years after the World Trade Center" before the Subcommittee on Technology,
technical/911report/chapter-13.3.txt:                after the World Trade Center," Feb. 24, 1998, p. 152; 8 U.S.C. � 1534(e)(1)(A). On
technical/911report/chapter-13.3.txt:                the terrorist from others around the world who had his or her name. In addition, the
technical/911report/chapter-13.3.txt:                panels' work was largely secret, the intelligence community's annual worldwide
technical/911report/chapter-13.4.txt:            33. For KSM's learning from the first World Trade Center bombing and his interest in
technical/911report/chapter-13.4.txt:                World Trade Center and CIA, see Intelligence report, interrogation of KSM, Feb. 19,
technical/911report/chapter-13.4.txt:                targets, including the World Trade Center, with hijacked commercial airliners flown
technical/911report/chapter-13.4.txt:                operatives around the world by obtaining fraudulent documents, arranging visas (real
technical/911report/chapter-13.4.txt:                other, high-priority activities, such as worldwide disruptions. The telescope
technical/911report/chapter-13.4.txt:                world, sometimes-as in Thumairy's case-with diplomatic status in the host country.
technical/911report/chapter-13.4.txt:                "two Saudis" around Los Angeles and to San Diego's Sea World after being introduced
technical/911report/chapter-13.5.txt:                trip, Ghalyoun videotaped a number of U.S. landmarks, including the World Trade
technical/911report/chapter-13.5.txt:            1. For the WTC's layout, see Port Authority diagrams, "World Trade Center Concourse
technical/911report/chapter-13.5.txt:                of office space, see Federal Emergency Management Agency (FEMA) report, "World Trade
technical/911report/chapter-13.5.txt:                report,"World Trade Center Building Performance Study," undated. In addition, the
technical/911report/chapter-13.5.txt:                Chief of Department, Anthony L. Fusco," in William Manning, ed., The World Trade
technical/911report/chapter-13.5.txt:                "Report of the World Trade Center Review Committee," 1995, p. 4. For generators'
technical/911report/chapter-13.5.txt:                ed., The World Trade Center Bombing, p. 11. For the evacuation time, see PANYNJ
technical/911report/chapter-13.5.txt:                figure of 15 hours, see "World Trade Center Bombing," NY Cop Online Magazine, Dec.
technical/911report/chapter-13.5.txt:                ed., The World Trade Center Bombing, p. 11.
technical/911report/chapter-13.5.txt:                World Trade Center," June 28, 2004. On people alive on the 92nd floor and above
technical/911report/chapter-13.5.txt:                in Manning, ed., The World Trade Center Bombing, p. 94.
technical/911report/chapter-13.5.txt:                and Fire Safety Investigation of the World Trade Center," June 18, 2004, appendix
technical/911report/chapter-13.5.txt:                preparations for the International Monetary Fund and the World Bank meetings, see
technical/911report/chapter-13.5.txt:                (online at http://worldtradeaftermath.com/wta/contacts/companies_list.asp?
technical/911report/chapter-13.5.txt:            13. The collapse of the World Trade Center towers on the morning of September 11
technical/911report/chapter-13.5.txt:                World Trade Center Collapse: Challenges, Successes, and Areas for Improvement," Aug.
technical/911report/chapter-13.5.txt:                Check, "Asbestos Alert; How much of the chemical does the World Trade Center
technical/911report/chapter-13.5.txt:                Inspector General report, "EPA's Response to the World Trade Center Collapse,"Aug.
technical/911report/chapter-13.5.txt:                World War II (Oxford Univ. Press, 1988), p. 215.
technical/911report/chapter-13.5.txt:                Arab Terrorists to Attack the World Trade Center in New York," Aug. 12, 1998. An FAA
technical/911report/chapter-13.5.txt:            19. FAA memo, Office of Civil Aviation Security Intelligence, "Usama Bin Ladin/World
technical/911report/chapter-13.5.txt:                virtually any building located anywhere in the world." DOJ memo, Robert D. to
technical/911report/chapter-13.5.txt:                born about 1940, is a product of the modern world, influenced by Marxist-Leninist
technical/911report/chapter-13.5.txt:            4. Opening the Islamic Conference of Muslim leaders from around the world on October
technical/911report/chapter-13.5.txt:                but instead planning a thoughtful, long-term strategy to defeat their worldwide
technical/911report/chapter-13.5.txt:                world by proxy. They get others to fight and die for them." Speech at the Opening of
technical/911report/chapter-13.5.txt:                Attitudes Project report, Views of a Changing World: June 2003 (Pew Research Center
technical/911report/chapter-13.5.txt:                But World Embraces Democratic Values and Free Markets," June 3, 2003 (online at
technical/911report/chapter-13.5.txt:            28. Testimony of George Tenet, "The Worldwide Threat 2004: Challenges in a Changing
technical/911report/chapter-13.5.txt:                would offer an integrated depiction of groups like al Qaeda or Hezbollah worldwide,
technical/911report/chapter-2.txt:                "World Islamic Front." A fatwa is normally an interpretation of Islamic law by a
technical/911report/chapter-2.txt:                in the world today and the worst terrorists are the Americans. Nothing could stop
technical/911report/chapter-2.txt:                destroy America and bring the world to Islam.
technical/911report/chapter-2.txt:            BIN LADIN'S APPEAL IN THE ISLAMIC WORLD 
technical/911report/chapter-2.txt:                shared in the Muslim world. He inveighed against the presence of U.S. troops in
technical/911report/chapter-2.txt:                over all aspects of life. Periodically, the Islamic world has seen surges of what,
technical/911report/chapter-2.txt:            Bin Ladin's Worldview Despite his claims to universal leadership, Bin Ladin offers an
technical/911report/chapter-2.txt:                more tranquil world, he offers his "Caliphate" as an imagined alternative to today's
technical/911report/chapter-2.txt:                uncertainty. For others, he offers simplistic conspiracies to explain their world.
technical/911report/chapter-2.txt:            Three basic themes emerge from Qutb's writings. First, he claimed that the world was
technical/911report/chapter-2.txt:            History and Political Context Few fundamentalist movements in the Islamic world
technical/911report/chapter-2.txt:                the overwhelmingly secular struggles for independence after World War I.
technical/911report/chapter-2.txt:                progress. After gaining independence from Western powers following World War II, the
technical/911report/chapter-2.txt:            The bankruptcy of secular, autocratic nationalism was evident across the Muslim world
technical/911report/chapter-2.txt:                revival movements gained followers across the Muslim world, but failed to secure
technical/911report/chapter-2.txt:                common problem throughout the Muslim world: a large, steadily increasing population
technical/911report/chapter-2.txt:                attention to the rest of the world's thought, history, and culture. The secular
technical/911report/chapter-2.txt:                around the world. It's a faith that has made brothers and sisters of every race.
technical/911report/chapter-2.txt:            Finally, Bin Ladin had another advantage: a substantial, worldwide organization. By
technical/911report/chapter-2.txt:            Young Muslims from around the world flocked to Afghanistan to join as volunteers in
technical/911report/chapter-2.txt:                increasingly complex, almost worldwide organization. This organization included a
technical/911report/chapter-2.txt:                world markets to buy arms and supplies for the mujahideen, or "holy warriors."
technical/911report/chapter-2.txt:                the world, including the United States. Some were set up by Islamic extremists or
technical/911report/chapter-2.txt:                and for preparing the mujahideen to fight anywhere in the world. Azzam, by contrast,
technical/911report/chapter-2.txt:                would let Bin Ladin use Sudan as a base for worldwide business operations and for
technical/911report/chapter-2.txt:                already-established Third World Relief Agency (TWRA) headquartered in Vienna, whose
technical/911report/chapter-2.txt:                members of someone else's organization-were traveling around the world and joining
technical/911report/chapter-2.txt:                cloudy are the 1993 bombing of the World Trade Center, a plot that same year to
technical/911report/chapter-2.txt:                corner of the Muslim world. His vision mirrored that of Sudan's Islamist leader,
technical/911report/chapter-2.txt:                together with strains in the world economy, hurt Sudan's currency. Some of Bin
technical/911report/chapter-2.txt:                world. And he had strengthened the internal ties in his own organization.
technical/911report/chapter-2.txt:                who were subsequently convicted in the February 1993 attack on the World Trade
technical/911report/chapter-2.txt:                Ladin said that the World Islamic Front for jihad against "Jews and Crusaders" had
technical/911report/chapter-3.txt:            FROM THE OLD TERRORISM TO THE NEW: THE FIRST WORLD TRADE CENTER
technical/911report/chapter-3.txt:                towers of the World Trade Center. This was not a suicide attack. The terrorists
technical/911report/chapter-3.txt:                around the world. The National Security Agency (NSA), the huge Defense Department
technical/911report/chapter-3.txt:                oppressor of Muslims worldwide and asserting that it was their religious duty to
technical/911report/chapter-3.txt:                to the World Trade Center bombing and other plots. An unfortunate consequence of
technical/911report/chapter-3.txt:            Third, the successful use of the legal system to address the first World Trade Center
technical/911report/chapter-3.txt:            The FBI's domestic intelligence gathering dates from the 1930s. With World War II
technical/911report/chapter-3.txt:                budget request to Congress after the 1993 World Trade Center bombing, he stated that
technical/911report/chapter-3.txt:            Commissioner Meissner responded in 1993 to the World Trade Center bombing by
technical/911report/chapter-3.txt:                World Trade Center bombing, to enlist local officers, as well as other agency
technical/911report/chapter-3.txt:                the February 1993 bombing of the World Trade Center and the April 1995 bombing of
technical/911report/chapter-3.txt:                hijacked a U.S.commercial aircraft anywhere in the world since 1986.
technical/911report/chapter-3.txt:            The emergence of the World Wide Web has given terrorists a much easier means of
technical/911report/chapter-3.txt:                in World War II after having first thought the FBI might take that role. The father
technical/911report/chapter-3.txt:            At the end of World War II, to Donovan's disappointment, President Harry Truman
technical/911report/chapter-3.txt:                new issues. Inevitably, some parts of the world and some collection targets were not
technical/911report/chapter-3.txt:                relations with the rest of the world. The National Security Council was created in
technical/911report/chapter-3.txt:            State Department consular officers around the world, it should not be forgotten, were
technical/911report/chapter-3.txt:                1990s, State had created a worldwide, real-time electronic database of visa, law
technical/911report/chapter-3.txt:                wounded, 18 were killed, and the world's television screens showed images of an
technical/911report/chapter-3.txt:                captured abroad much later.) Only a month afterward came the World Trade Center
technical/911report/chapter-3.txt:                worldwide, including one in New York. Neither the FBI nor the CIA had ever heard of
technical/911report/chapter-3.txt:                following World War II. The Congressional Reorganization Act of 1946 created the
technical/911report/chapter-3.txt:                annual worldwide threat hearing, held eight; its House counterpart held perhaps two
technical/911report/chapter-3.txt:                Islamic' regimes worldwide." After the department designated Sudan a state sponsor
technical/911report/chapter-3.txt:                operations against U.S. interests worldwide and was actively trying to obtain
technical/911report/chapter-3.txt:                authorized worldwide covert action against terrorism and probably provided adequate
technical/911report/chapter-3.txt:                did not emphasize the existence of a structured worldwide organization gearing up to
technical/911report/chapter-3.txt:                Serbia in 1999, in each case provoking worldwide criticism, Deputy National Security
technical/911report/chapter-3.txt:                unconcerned about commerce with the outside world. Omar had virtually no diplomatic
technical/911report/chapter-3.txt:                the Taliban's only travel and financial outlets to the outside world, to break off
technical/911report/chapter-3.txt:                worldwide. It announced a program for hiring and training better officers with
technical/911report/chapter-5.txt:                Within this structure, al Qaeda's worldwide terrorist operations relied heavily on
technical/911report/chapter-5.txt:                in the first World Trade Center bombing. According to KSM, he learned of Ramzi
technical/911report/chapter-5.txt:            Yousef 's instant notoriety as the mastermind of the 1993 World Trade Center bombing
technical/911report/chapter-5.txt:            KSM continued to travel among the worldwide jihadist community after Yousef 's
technical/911report/chapter-5.txt:            At the meeting, KSM briefed Bin Ladin and Atef on the first World Trade Center
technical/911report/chapter-5.txt:                returned to Pakistan following the 1993 World Trade Center bombing. Like Yousef, KSM
technical/911report/chapter-5.txt:            KSM claims that the earlier bombing of the World Trade Center taught him that bombs
technical/911report/chapter-5.txt:                striking the World Trade Center and CIA headquarters as early as 1995.
technical/911report/chapter-5.txt:                governments in the Arab world. Beyond KSM's rationalizations about targeting the
technical/911report/chapter-5.txt:                Pentagon, and the World Trade Center. According to KSM, Bin Ladin wanted to destroy
technical/911report/chapter-5.txt:                the White House and the Pentagon, KSM wanted to strike the World Trade Center, and
technical/911report/chapter-5.txt:                be in the air at the same time in different parts of the world. They used the game
technical/911report/chapter-5.txt:                world and the media, to polemics against governments of the Arab world. To him,
technical/911report/chapter-5.txt:                be a "Jewish world conspiracy." He proclaimed that the highest duty of every Muslim
technical/911report/chapter-5.txt:                world "in a natural way."
technical/911report/chapter-5.txt:                including a preliminary list of approved targets: the World Trade Center, the
technical/911report/chapter-6.txt:                disruption efforts around the world had achieved some successes, the core of Bin
technical/911report/chapter-6.txt:                period." The State Department issued a worldwide threat advisory to its posts
technical/911report/chapter-6.txt:                seizing the funds of a clandestine worldwide organization like al Qaeda. Although
technical/911report/chapter-6.txt:                might inflame the Islamic world and increase support for the Taliban. Defense
technical/911report/chapter-6.txt:                America's perennially troubled public diplomacy efforts in the Muslim world, where
technical/911report/chapter-7.txt:                contacts with Iran and the Iranian-supported worldwide terrorist organization
technical/911report/chapter-7.txt:                that passes New York landmarks like the World Trade Center. Heavy traffic in the
technical/911report/chapter-7.txt:                discussed before Atta left Afghanistan in early 2000-the World Trade Center, the
technical/911report/chapter-7.txt:                the Capitol, and that both Atta and Shehhi would hit the World Trade Center. If any
technical/911report/chapter-7.txt:                not strike the World Trade Center, he planned to crash his aircraft directly into
technical/911report/chapter-7.txt:                referred to the World Trade Center, "arts" the Pentagon,"law" the Capitol, and
technical/911report/chapter-7.txt:                generating rumors throughout the worldwide jihadist community. Bin Ladin routinely
technical/911report/chapter-8.txt:                and updated its worldwide public warning. In June, the State Department initiated
technical/911report/chapter-8.txt:                indicating that they would cause the world to be in turmoil and that they would
technical/911report/chapter-8.txt:            Tenet told us that in his world "the system was blinking red." By late July, Tenet
technical/911report/chapter-8.txt:                    followers would follow the example of World Trade Center bomber Ramzi Yousef and
technical/911report/chapter-8.txt:                taking a plane and crashing into the World Trade Center." The headquarters agent
technical/911report/chapter-8.txt:                were alerted across the world. Many were doing everything they possibly could to
technical/911report/chapter-9.txt:                World Trade Center rested not with national policymakers but with private firms and
technical/911report/chapter-9.txt:            The World Trade Center.
technical/911report/chapter-9.txt:            The World Trade Center (WTC) complex was built for the Port Authority of New York and
technical/911report/chapter-9.txt:                of America, New York City and specifically the World Trade Center had been the
technical/911report/chapter-9.txt:                and exposed vulnerabilities in the World Trade Center's and the city's emergency
technical/911report/chapter-9.txt:                Port Authority World Trade Department employees-including those not on the
technical/911report/chapter-9.txt:                Authority's nine facilities, including the World Trade Center.
technical/911report/chapter-9.txt:                overall response to an The World Trade Center Radio Repeater System Rendering by
technical/911report/chapter-9.txt:                    1 World Trade Center (the North Tower) at 8:46 until the South Tower was hit
technical/911report/chapter-9.txt:                    2 World Trade Center (the South Tower) at 9:03 until the collapse of the South
technical/911report/chapter-9.txt:                airplane crash at the World Trade Center. The air traffic controllers had been
technical/911report/chapter-9.txt:                vicinity of the World Trade Center and evacuating civilians from those
technical/911report/chapter-9.txt:                civilians in the World Trade Center complex, because of the magnitude of the
technical/911report/chapter-9.txt:                World restaurant on the 106th floor, from which calls had been made to the PAPD
technical/911report/chapter-9.txt:                at 2 World Financial Center and were not available to influence FDNY operations for
technical/911report/chapter-9.txt:                World Trade Center that same morning included catastrophic damage 1,000 feet above
technical/911report/chapter-9.txt:                safety at the annual meetings of the International Monetary Fund and the World Bank
technical/911report/chapter-9.txt:                experience of the civilians at the World Trade Center on 9/11.
technical/911report/chapter-9.txt:                disaster strike. Clearly, many building occupants in the World Trade Center did not
technical/911report/chapter-9.txt:                World Trade Center attacks, the FDNY as an institution proved incapable of
technical/911report/chapter-9.txt:            The first responders of today live in a world transformed by the attacks on 9/11.
technical/911report/preface.txt:                enemy rallies broad support in the Arab and Muslim world by demanding redress of
technical/911report/preface.txt:                purpose is to rid the world of religious and political pluralism, the plebiscite,
```
We can see that even I call grep -i "World", it printed also the lower case "world". 

[Second Example]
```
seosonghee@seosonghuis-MacBook-Air docsearch %  grep -i "New York" technical/911report/*.txt                 
technical/911report/chapter-1.txt:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
technical/911report/chapter-1.txt:    At 8:41, in American's operations center, a colleague told Marquis that the air traffic controllers declared Flight 11 a hijacking and "think he's [American 11] headed toward Kennedy [airport in New York City]. They're moving everybody out of the way. They seem to have him on a primary radar. They seem to think that he is descending."
technical/911report/chapter-1.txt:    At 8:46:40, American 11 crashed into the North Tower of the World Trade Center in New York City.
technical/911report/chapter-1.txt:    The first operational evidence that something was abnormal on United 175 came at 8:47, when the aircraft changed beacon codes twice within a minute. At 8:51, the flight deviated from its assigned altitude, and a minute later New York air traffic controllers began repeatedly and unsuccessfully trying to contact it.
technical/911report/chapter-1.txt:    At 8:58, the flight took a heading toward New York City.
technical/911report/chapter-1.txt:    At least two callers from the flight reported that the hijackers knew that passengers were making calls but did not seem to care. It is quite possible Jarrah knew of the success of the assault on the World Trade Center. He could have learned of this from messages being sent by United Airlines to the cockpits of its transcontinental flights, including Flight 93, warning of cockpit intrusion and telling of the New York attacks. But even without them, he would certainly have understood that the attacks on the World Trade Center would already have unfolded, given Flight 93's tardy departure from Newark. If Jarrah did know that the passengers were making calls, it might not have occurred to him that they were certain to learn what had happened in New York, thereby defeating his attempts at deception.
technical/911report/chapter-1.txt:    FAA Control Centers often receive information and make operational decisions independently of one another. On 9/11, the four hijacked aircraft were monitored mainly by the centers in Boston, New York, Cleveland, and Indianapolis. Each center thus had part of the knowledge of what was going on across the system. What Boston knew was not necessarily known by centers in New York, Cleveland, or Indianapolis, or for that matter by the Command Center in Herndon or by FAA headquarters in Washington.
technical/911report/chapter-1.txt:    In the United States, NORAD is divided into three sectors. On 9/11, all the hijacked aircraft were in NORAD's Northeast Air Defense Sector (also known as NEADS), which is based in Rome, New York. That morning NEADS could call on two alert sites, each with one pair of ready fighters: Otis Air National Guard Base in Cape Cod, Massachusetts, and Langley Air Force Base in Hampton, Virginia.
technical/911report/chapter-1.txt:    Between 8:25 and 8:32, in accordance with the FAA protocol, Boston Center managers started notifying their chain of command that American 11 had been hijacked. At 8:28, Boston Center called the Command Center in Herndon to advise that it believed American 11 had been hijacked and was heading toward New York Center's airspace.
technical/911report/chapter-1.txt:    The Herndon Command Center immediately established a teleconference between Boston, New York, and Cleveland Centers so that Boston Center could help the others understand what was happening.
technical/911report/chapter-1.txt:    FAA: Hi. Boston Center TMU [Traffic Management Unit], we have a problem here. We have a hijacked aircraft headed towards New York, and we need you guys to, we need someone to scramble some F-16s or something up there, help us out.
technical/911report/chapter-1.txt:    NEADS ordered to battle stations the two F-15 alert aircraft at Otis Air Force Base in Falmouth, Massachusetts, 153 miles away from New York City. The air defense of America began with this call.
technical/911report/chapter-1.txt:    Radar data show the Otis fighters were airborne at 8:53. Lacking a target, they were vectored toward military-controlled airspace off the Long Island coast. To avoid New York area air traffic and uncertain about what to do, the fighters were brought down to military airspace to "hold as needed." From 9:09 to 9:13, the Otis fighters stayed in this holding pattern.
technical/911report/chapter-1.txt:FAA Awareness. One of the last transmissions from United Airlines Flight 175 is, in retrospect, chilling. By 8:40, controllers at the FAA's New York Center were seeking information on American 11. At approximately 8:42, shortly after entering New York Center's airspace, the pilot of United 175 broke in with the following transmission:
technical/911report/chapter-1.txt:    UAL 175: New York UAL 175 heavy.
technical/911report/chapter-1.txt:    Minutes later, United 175 turned southwest without clearance from air traffic control. At 8:47, seconds after the impact of American 11, United 175's transponder code changed, and then changed again. These changes were not noticed for several minutes, however, because the same New York Center controller was assigned to both American 11 and United 175. The controller knew American 11 was hijacked; he was focused on searching for it after the aircraft disappeared at 8:46.
technical/911report/chapter-1.txt:    At 8:48, while the controller was still trying to locate American 11, a New York Center manager provided the following report on a Command Center teleconference about American 11:
technical/911report/chapter-1.txt:    Manager, New York Center: Okay. This is New York Center. We're watching the airplane. I also had conversation with American Airlines, and they've told us that they believe that one of their stewardesses was stabbed and that there are people in the cockpit that have control of the aircraft, and that's all the information they have right now.
technical/911report/chapter-1.txt:    The New York Center controller and manager were unaware that American 11 had already crashed.
technical/911report/chapter-1.txt:    Another commercial aircraft in the vicinity then radioed in with "reports over the radio of a commuter plane hitting the World Trade Center." The controller spent the next several minutes handing off the other flights on his scope to other controllers and moving aircraft out of the way of the unidentified aircraft (believed to be United 175) as it moved southwest and then turned northeast toward New York City.
technical/911report/chapter-1.txt:    At about 8:55, the controller in charge notified a New York Center manager that she believed United 175 had also been hijacked. The manager tried to notify the regional managers and was told that they were discussing a hijacked aircraft (presumably American 11) and refused to be disturbed. At 8:58, the New York Center controller searching for United 175 told another New York controller "we might have a hijack over here, two of them."
technical/911report/chapter-1.txt:    Between 9:01 and 9:02, a manager from New York Center told the Command Center in Herndon:
technical/911report/chapter-1.txt:    Manager, New York Center: We have several situations going on here. It's escalating big, big time. We need to get the military involved with us. . . . We're, we're involved with something else, we have other aircraft that may have a similar situation going on here.
technical/911report/chapter-1.txt:    The "other aircraft" referred to by New York Center was United 175. Evidence indicates that this conversation was the only notice received by either FAA headquarters or the Herndon Command Center prior to the second crash that there had been a second hijacking.
technical/911report/chapter-1.txt:    While the Command Center was told about this "other aircraft" at 9:01, New York Center contacted New York terminal approach control and asked for help in locating United 175.
technical/911report/chapter-1.txt:    Boston Center: It sounds like, we're talking to New York, that there's another one aimed at the World Trade Center.
technical/911report/chapter-1.txt:    Boston Center immediately advised the New England Region that it was going to stop all departures at airports under its control. At 9:05, Boston Center confirmed for both the FAA Command Center and the New England Region that the hijackers aboard American 11 said "we have planes." At the same time, New York Center declared "ATC zero"-meaning that aircraft were not permitted to depart from, arrive at, or travel through New York Center's airspace until further notice.
technical/911report/chapter-1.txt:    Within minutes of the second impact, Boston Center instructed its controllers to inform all aircraft in its airspace of the events in New York and to advise aircraft to heighten cockpit security. Boston Center asked the Herndon Command Center to issue a similar cockpit security alert nationwide. We have found no evidence to suggest that the Command Center acted on this request or issued any type of cockpit security alert.
technical/911report/chapter-1.txt:Military Notification and Response. The first indication that the NORAD air defenders had of the second hijacked aircraft, United 175, came in a phone call from New York Center to NEADS at 9:03. The notice came at about the time the plane was hitting the South Tower.
technical/911report/chapter-1.txt:    Because the Otis fighters had expended a great deal of fuel in flying first to military airspace and then to New York, the battle commanders were concerned about refueling. NEADS considered scrambling alert fighters from Langley Air Force Base in Virginia to New York, to provide backup. The Langley fighters were placed on battle stations at 9:09.137 NORAD had no indication that any other plane had been hijacked.
technical/911report/chapter-1.txt:    The controller tracking American 77 told us he noticed the aircraft turning to the southwest, and then saw the data disappear. The controller looked for primary radar returns. He searched along the plane's projected flight path and the airspace to the southwest where it had started to turn. No primary targets appeared. He tried the radios, first calling the aircraft directly, then the airline. Again there was nothing. At this point, the Indianapolis controller had no knowledge of the situation in New York. He did not know that other aircraft had been hijacked. He believed American 77 had experienced serious electrical or mechanical failure, or both, and was gone.
technical/911report/chapter-1.txt:    After consulting with NEADS command, the crew commander issued the order at 9:23:"Okay . . . scramble Langley. Head them towards the Washington area. . . . [I]f they're there then we'll run on them. . . . These guys are smart." That order was processed and transmitted to Langley Air Force Base at 9:24. Radar data show the Langley fighters airborne at 9:30. NEADS decided to keep the Otis fighters over New York. The heading of the Langley fighters was adjusted to send them to the Baltimore area. The mission crew commander explained to us that the purpose was to position the Langley fighters between the reported southbound American 11 and the nation's capital.
technical/911report/chapter-1.txt:    Most federal agencies learned about the crash in New York from CNN.
technical/911report/chapter-1.txt:    When they learned a second plane had struck the World Trade Center, nearly everyone in the White House told us, they immediately knew it was not an accident. The Secret Service initiated a number of security enhancements around the White House complex. The officials who issued these orders did not know that there were additional hijacked aircraft, or that one such aircraft was en route to Washington. These measures were precautionary steps taken because of the strikes in New York.
technical/911report/chapter-1.txt:    On the morning of September 11, Secretary Rumsfeld was having breakfast at the Pentagon with a group of members of Congress. He then returned to his office for his daily intelligence briefing. The Secretary was informed of the second strike in New York during the briefing; he resumed the briefing while awaiting more information. After the Pentagon was struck, Secretary Rumsfeld went to the parking lot to assist with rescue efforts.
technical/911report/chapter-1.txt:    while the children continued reading. He then returned to a holding room shortly before 9:15, where he was briefed by staff and saw television coverage. He next spoke to Vice President Cheney, Dr. Rice, New York Governor George Pataki, and FBI Director Robert Mueller. He decided to make a brief statement from the school before leaving for the airport. The Secret Service told us they were anxious to move the President to a safer location, but did not think it imperative for him to run out the door.
technical/911report/chapter-1.txt:    In upstate New York, NEADS personnel first learned of the shootdown order from this message: Floor Leadership: You need to read this. . . . The Region Commander has declared that we can shoot down aircraft that do not respond to our direction. Copy that?
technical/911report/chapter-1.txt:    The NEADS commander told us he did not pass along the order because he was unaware of its ramifications. Both the mission commander and the senior weapons director indicated they did not pass the order to the fighters circling Washington and New York because they were unsure how the pilots would, or should, proceed with this guidance. In short, while leaders in Washington believed that the fighters above them had been instructed to "take out" hostile aircraft, the only orders actually conveyed to the pilots were to "ID type and tail."
technical/911report/chapter-1.txt:    At 10:02 that morning, an assistant to the mission crew commander at NORAD's Northeast Air Defense Sector in Rome, New York, was working with his colleagues on the floor of the command center. In a brief moment of reflection, he was recorded remarking that "This is a new type of war."
technical/911report/chapter-10.txt:                    provide $20 billion for New York City, in addition to the $20 billion his budget
technical/911report/chapter-12.txt:                state and local governments, we heard-especially in New York-about imbalances in the
technical/911report/chapter-12.txt:                    Washington, D.C., and New York City are certainly at the top of any such list.
technical/911report/chapter-12.txt:                    safety purposes. Furthermore, high-risk urban areas such as New York City and
technical/911report/chapter-13.1.txt:                Minneapolis, and New York displayed initiative in pressing their investigations.
technical/911report/chapter-13.2.txt:                FBI-Federal Bureau of Investigation; FDNY-Fire Department of New York; GAO-General
technical/911report/chapter-13.2.txt:                NTSB-National Transportation Safety Board; NYPD-New York Police Department;
technical/911report/chapter-13.2.txt:                OEM-Office of Emergency Management, City of New York; PANYNJ or Port Authority-Port
technical/911report/chapter-13.2.txt:                Authority of New York and New Jersey; PAPD-Port Authority Police Department;
technical/911report/chapter-13.2.txt:                diverted to JFK Airport in New York. The event lasted for 11 hours and was resolved
technical/911report/chapter-13.2.txt:                AAL11; New York, NY; September 11, 2001," Feb. 15, 2002, p. 7.
technical/911report/chapter-13.2.txt:            109. FAA memo, "FullTranscript; Aircraft Accident; AAL11; New York, NY; September
technical/911report/chapter-13.2.txt:            111. FAA memo, "FullTranscript; Aircraft Accident; AAL11; New York, NY; September
technical/911report/chapter-13.2.txt:            113. FAA memo, "FullTranscript; Aircraft Accident; AAL11; New York, NY; September
technical/911report/chapter-13.2.txt:            114. FAA memo, "FullTranscript; Aircraft Accident; AAL11; New York, NY; September
technical/911report/chapter-13.2.txt:            115. FAA memo, "FullTranscript; Aircraft Accident; AAL11; New York, NY; September
technical/911report/chapter-13.2.txt:            117. For the distance between Otis Air Force Base and New York City, see William
technical/911report/chapter-13.2.txt:                before they headed for New York. NEADS controllers were simultaneously working with
technical/911report/chapter-13.2.txt:                combat air patrol over New York, and they immediately headed for New York City. See
technical/911report/chapter-13.2.txt:            122. FAA memo, "Full Transcript; Aircraft Accident; UAL175; New York, NY; September
technical/911report/chapter-13.2.txt:            123. FAA audio file, New York Center, position R42, 8:42-8:45; FAA memo, "Full
technical/911report/chapter-13.2.txt:                Transcript; Aircraft Accident; UAL175; New York, NY; September 11, 2001,"May 8,
technical/911report/chapter-13.2.txt:                1, 2003); FAA memo,"Full Transcript; Aircraft Accident; UAL175; New York, NY;
technical/911report/chapter-13.2.txt:            124. FAA audio file, Herndon Command Center, New York Center position, line 5114,
technical/911report/chapter-13.2.txt:            125. FAA memo, "Full Transcript; Aircraft Accident; UAL175; New York, NY; September
technical/911report/chapter-13.2.txt:                FAA memo, "Full Transcript; Aircraft Accident; UAL175; New York, NY; September 11,
technical/911report/chapter-13.2.txt:                also FAA memo,"Full Transcript; Aircraft Accident; UAL175; New York, NY; September
technical/911report/chapter-13.2.txt:            129. FAA memo, "Full Transcript; Aircraft Accident; UAL175; New York, NY; September
technical/911report/chapter-13.2.txt:            130." N90 [New York Terminal Radar Approach] controller stated 'at approximately 9:00
technical/911report/chapter-13.2.txt:            131. FAA audio file, Herndon Command Center, New York Center position, line 5114,
technical/911report/chapter-13.2.txt:                military airspace and then to New York, the battle commanders were concerned about
technical/911report/chapter-13.2.txt:                protect New York City." Filson, Air War Over America, p. 60.
technical/911report/chapter-13.2.txt:                2003, pp. 10, 13; FAA audio file, Herndon Command Center, New York Center position,
technical/911report/chapter-13.2.txt:                second attack in New York, a senior Secret Service agent charged with coordinating
technical/911report/chapter-13.3.txt:                New York.
technical/911report/chapter-13.3.txt:                Warriors Learned to Hate," New York Times, June 18, 2004, p. A31.
technical/911report/chapter-13.3.txt:                people as possible co-conspirators in the New York City landmarks plot. Ali Mohamed,
technical/911report/chapter-13.3.txt:                visa at New York City on September 9, 1991. INS alien file, No. A72215823, Sept. 9,
technical/911report/chapter-13.3.txt:                Slipped Away Long Before Sept. 11 Attack," New York Times, Mar. 8, 2003, p. A12.
technical/911report/chapter-13.3.txt:                attack was determined to be al Qaeda-related, responsibility shifted to the New York
technical/911report/chapter-13.3.txt:                In addition, the U.S. Attorney for the Southern District of New York was given an
technical/911report/chapter-13.3.txt:                of city noncooperation, see New York Mayor Ed Koch's 1987 order prohibiting city
technical/911report/chapter-13.3.txt:                2004). On the New York JTTF, see Mary Jo White, "Prosecuting Terrorism in New York,"
technical/911report/chapter-13.4.txt:                Bernstein, "Germans Free Moroccan Convicted of a 9/11 Role," New York Times, Apr. 8,
technical/911report/chapter-13.4.txt:                Ibrahim,"Saudis Strip Citizenship from Backers of Militants," New York Times, Apr.
technical/911report/chapter-13.4.txt:                New York Times, Oct. 27, 1999, p. A1. The inability to freeze funds is attributed in
technical/911report/chapter-13.4.txt:                going to New York City, see FBI report, "Hijackers Timeline," Dec. 5, 2003 (May 30,
technical/911report/chapter-13.4.txt:                in a series of short-term rentals in New York City. Ibid. (June 19, 2000, entry
technical/911report/chapter-13.4.txt:                take their return flight to New York, and there are no travel records indicating how
technical/911report/chapter-13.5.txt:            The remaining hijackers entered the United States through New York. Salem al Hazmi
technical/911report/chapter-13.5.txt:                a co-worker in Indiana who had never been to New York and wanted to see what it
technical/911report/chapter-13.5.txt:                looked like. The picture taker was in New York to obtain further information
technical/911report/chapter-13.5.txt:                portions of the FBI's New York Field Office. Before going into the building the
technical/911report/chapter-13.5.txt:                Attorney's Office for the Southern District of New York. See NSA memo, Joan R. to
technical/911report/chapter-13.5.txt:                Product to U.S. Attorney's Office/Southern District of New York,"Aug. 30, 2000.
technical/911report/chapter-13.5.txt:                2000, pursuant to concerns of the FISA Court, the New York Field Office began
technical/911report/chapter-13.5.txt:                applied to this situation, there was in fact an exception in place for New York. DOJ
technical/911report/chapter-13.5.txt:                the chief division counsel in New York.
technical/911report/chapter-13.5.txt:                Southern District of New York from Part B of the 1995 procedures, so they did not
technical/911report/chapter-13.5.txt:                Heathrow Airport to New York's John F. Kennedy Airport; and he was also particularly
technical/911report/chapter-13.5.txt:                District of New York, told us that based on her review of the evidence known
technical/911report/chapter-13.5.txt:            6. For the towers' loss of power and the other effects, see New York City report,
technical/911report/chapter-13.5.txt:            14. See Port Authority Police Department (PAPD) report, "Port Authority of New York
technical/911report/chapter-13.5.txt:                2001, New York provided its firefighters with new digital radios. The procurement
technical/911report/chapter-13.5.txt:            26. For civilian fatalities, see New York City press release, Office of the Mayor
technical/911report/chapter-13.5.txt:                epidemic in its early stages), live video feeds from New York Harbor and city
technical/911report/chapter-13.5.txt:            29. New York City memo, "Direction and Control of Emergencies in the City of New
technical/911report/chapter-13.5.txt:            143. New York City Police Museum interview of Kenneth Winkler, Apr. 17, 2003
technical/911report/chapter-13.5.txt:            188. According to the number of death certificates issued by the New York City
technical/911report/chapter-13.5.txt:                nonterrorist occupants of the hijacked aircraft. New York City Office of the Chief
technical/911report/chapter-13.5.txt:                "Washington Is Seeking Support to Handle Protests at 2 Meetings," New York Times,
technical/911report/chapter-13.5.txt:                2004. For the updated death certificate information, see New York City report,"WTC
technical/911report/chapter-13.5.txt:                www.september11victims.com/september11Victims); New York Times, Portraits: 9/11/01:
technical/911report/chapter-13.5.txt:                Command at these incidents will be resolved by OEM." New York City memo, Office of
technical/911report/chapter-13.5.txt:                the Mayor,"Direction and Control of Emergencies in the City of New York," July 2001.
technical/911report/chapter-13.5.txt:            210. Eric Lipton, "A New Weapon for Firefighters," New York Times, May 30, 2004, p.
technical/911report/chapter-13.5.txt:                tests show "it is safe for New Yorkers to go back to work in New York's financial
technical/911report/chapter-13.5.txt:                8, 2004; Port Authority of New York and New Jersey, JFK Airport response to
technical/911report/chapter-13.5.txt:                Commission questions for the record, June 22, 2004; Port Authority of New York and
technical/911report/chapter-13.5.txt:            8. Tim Weiner, "U.S. Hard Put to Find Proof Bin Laden Directed Attacks," New York
technical/911report/chapter-13.5.txt:                Arab Terrorists to Attack the World Trade Center in New York," Aug. 12, 1998. An FAA
technical/911report/chapter-13.5.txt:            42. For the New York Times article about the Jordanian arrests, see Reuters, "Jordan
technical/911report/chapter-13.5.txt:                Seizes 13 and Links Them to Afghan Explosives Training," New York Times, Dec. 16,
technical/911report/chapter-13.5.txt:                New York Times, Dec. 18, 1999, p. A1. For television coverage, see Vanderbilt
technical/911report/chapter-13.5.txt:            18. Neil MacFarquhar, "Saudis Support a Jihad in Iraq, Not Back Home," New York
technical/911report/chapter-2.txt:                destroy landmarks in New York, and the 1995 Manila air plot to blow up a dozen U.S.
technical/911report/chapter-3.txt:            The New York Field Office of the FBI took control of the local investigation and, in
technical/911report/chapter-3.txt:                District of New York prosecuted and convicted multiple individuals, including Ajaj,
technical/911report/chapter-3.txt:                investigation. Because the New York Field Office indicted Bin Ladin prior to the
technical/911report/chapter-3.txt:                worked closely with the U.S. Attorney for the Southern District of New York to
technical/911report/chapter-3.txt:                was the Joint Terrorism Task Force (JTTF), first tried out in New York City in 1980
technical/911report/chapter-3.txt:                task force was managed by the New York Field Office of the FBI, and its existence
technical/911report/chapter-3.txt:                worldwide, including one in New York. Neither the FBI nor the CIA had ever heard of
technical/911report/chapter-3.txt:                suspicious links with Omar Abdel Rahman, the "Blind Sheikh" in the New York area,
technical/911report/chapter-3.txt:                FBI's New York Field Office and the U.S. Attorney for the Southern District of New
technical/911report/chapter-3.txt:                in a New York court. Meanwhile, the State Department was focused more on lessening
technical/911report/chapter-3.txt:                Kansi capture. From there, a CIA plane would take him to New York, an Arab capital,
technical/911report/chapter-3.txt:                District of New York, and her staff. Though "Jeff " also used the 30 percent success
technical/911report/chapter-3.txt:                impression from the New York briefing was that the chances of capturing Bin Ladin
technical/911report/chapter-3.txt:                indictment against Bin Ladin. The New York grand jury issued its sealed indictment a
technical/911report/chapter-3.txt:                and nerve gas was used in a New York subway two weeks later.
technical/911report/chapter-3.txt:                for the Southern District of New York unsealed its indictment of Bin Ladin, charging
technical/911report/chapter-3.txt:                        recent trial run at an unidentified New York airport. [-]
technical/911report/chapter-3.txt:                group agreed that New York airports should go to maximum security starting that
technical/911report/chapter-3.txt:                to distribute versions of the report to the FBI and FAA to pass to the New York
technical/911report/chapter-3.txt:                and more oversight of the screening process, at all three New York City area
technical/911report/chapter-3.txt:                D.C. or New York. After investigation, the FBI could find no information to support
technical/911report/chapter-3.txt:                report. The FAA alert at the New York area airports ended on January 31, 1999.
technical/911report/chapter-3.txt:                threat to a flight out of Los Angeles or New York.
technical/911report/chapter-5.txt:                economic and "Jewish" targets in New York City. Furthermore, during the summer of
technical/911report/chapter-5.txt:                Jewish movement centered in New York City that supposedly controlled the financial
technical/911report/chapter-6.txt:                also acquired new confederates. He promised to help a New York-based partner,
technical/911report/chapter-6.txt:                handling al Qaeda-related investigations, including John O'Neill in New York. As a
technical/911report/chapter-6.txt:                Bank of New York, were also frozen.
technical/911report/chapter-6.txt:                offices, including New York, Chicago, Detroit, San Diego, and Minneapolis. On a
technical/911report/chapter-6.txt:                the use of the Bank of New York by Russian money launderers to move millions of
technical/911report/chapter-7.txt:                from Brussels. He went to New York City and waited there for Mohamed Atta to join
technical/911report/chapter-7.txt:            Rababah, who had lived in Connecticut, New York, and New Jersey, told investigators
technical/911report/chapter-7.txt:                Orlando or Miami, Florida; Washington, D.C.; or New York. Those arriving in Florida
technical/911report/chapter-7.txt:                at John F. Kennedy International Airport in New York. Mihdhar gave his intended
technical/911report/chapter-7.txt:                address as the Marriott Hotel, New York City, but instead spent one night at another
technical/911report/chapter-7.txt:                New York hotel. He then joined the group of hijackers in Paterson, reuniting with
technical/911report/chapter-7.txt:                cross-country surveillance flights early in the summer. Shehhi flew from New York to
technical/911report/chapter-7.txt:                that passes New York landmarks like the World Trade Center. Heavy traffic in the
technical/911report/chapter-7.txt:                cross-country surveillance flight, Atta flew into New York. Rather than return
technical/911report/chapter-7.txt:                the streets of New York. Atta told Binalshibh that each pilot had volunteered for
technical/911report/chapter-7.txt:                nuclear facility he had seen during familiarization flights near New York-a target
technical/911report/chapter-8.txt:                attacks on London, Boston, and New York. Attorney General John Ashcroft was briefed
technical/911report/chapter-8.txt:                New York City. The reporting noted that operatives might opt to hijack an aircraft
technical/911report/chapter-8.txt:                the Yemenis' surveillance of a federal building in New York had been looked into in
technical/911report/chapter-8.txt:                the reference to hijackings, the alert in New York, the alleged casing of buildings
technical/911report/chapter-8.txt:                in New York, the threat phoned in to the embassy, or the fact that the FBI had
technical/911report/chapter-8.txt:                    cell in New York was recruiting Muslim-American youth for attacks.
technical/911report/chapter-8.txt:                that any such concerns had reached FBI personnel beyond the New York Field
technical/911report/chapter-8.txt:            June 2001: The Meeting in New York
technical/911report/chapter-8.txt:                to New York on June 11 to meet with the agents about the Cole case. "Jane" brought
technical/911report/chapter-8.txt:                application indicated that he intended to travel to New York, that Hazmi had
technical/911report/chapter-8.txt:                "Dave" knew the answers to questions, he would have volunteered them. The New York
technical/911report/chapter-8.txt:                visa two days after the CIA-FBI meeting in New York. He flew to New York City on
technical/911report/chapter-8.txt:                New York meeting with "Jane" and "Dave" but had not looked into the issues yet
technical/911report/chapter-8.txt:                application-listed New York as his destination. On August 21, she located the March
technical/911report/chapter-8.txt:                information indicated that Mihdhar had last arrived in New York, she began drafting
technical/911report/chapter-8.txt:                what is known as a lead for the FBI's New York Field Office. A lead relays
technical/911report/chapter-8.txt:                action be taken. She called an agent in New York to give him a "headsup" on the
technical/911report/chapter-8.txt:                matter, but her draft lead was not sent until August 28. Her email told the New York
technical/911report/chapter-8.txt:                few days later. He checked local New York databases for criminal record and driver's
technical/911report/chapter-8.txt:                on international terrorism squads in the New York Field Office, advising of the
technical/911report/chapter-8.txt:                headquarters saw the memo before September 11, and the New York Field Office took no
technical/911report/chapter-8.txt:                flight from London to New York. He was told that the FBI had arrested Moussaoui
technical/911report/chapter-9.txt:            The World Trade Center (WTC) complex was built for the Port Authority of New York and
technical/911report/chapter-9.txt:                New York City and America.
technical/911report/chapter-9.txt:                of America, New York City and specifically the World Trade Center had been the
technical/911report/chapter-9.txt:                to be impassable. Rescue efforts by the Fire Department of New York (FDNY) were
technical/911report/chapter-9.txt:                evacuated from the roof of the South Tower by New York Police Department (NYPD)
technical/911report/chapter-9.txt:            On 9/11, the principal first responders were from the Fire Department of New York,
technical/911report/chapter-9.txt:                the New York Police Department, the Port Authority Police Department (PAPD), and the
technical/911report/chapter-9.txt:            The New York Police Department.
technical/911report/chapter-9.txt:            The Fire Department of New York.
technical/911report/chapter-9.txt:            Between 1998 and 2000, fewer people died from fires in New York City than in any
technical/911report/chapter-9.txt:                the NYPD-and other data. A second purpose of the OEM was to improve New York City's
technical/911report/chapter-9.txt:                Emergencies in the City of New York." Its purpose was to eliminate "potential
technical/911report/chapter-9.txt:            Within minutes, New York City's 911 system was flooded with eyewitness accounts of
technical/911report/chapter-9.txt:            In the 17-minute period between 8:46 and 9:03 A.M. on September 11, New York City and
technical/911report/chapter-9.txt:                the Port Authority of New York and New Jersey had mobilized the largest rescue
technical/911report/chapter-9.txt:                New York City back on its feet.
technical/911report/chapter-9.txt:                the far more difficult task in New York. There was a single incident, and it was not
technical/911report/chapter-9.txt:            It is a fair inference, given the differing situations in New York City and Northern
technical/911report/chapter-9.txt:                the attacks on 9/11 was necessarily improvised. In New York, the FDNY, NYPD, the
technical/911report/chapter-9.txt:                and Control of Emergencies in the City of New York." The directive designated, for
technical/911report/chapter-9.txt:                the possibility of imminent additional terrorist attacks throughout New York City.
technical/911report/chapter-9.txt:            If New York and other major cities are to be prepared for future terrorist attacks,
technical/911report/chapter-9.txt:            In May 2004, New York City adopted an emergency response plan that expressly
technical/911report/preface.txt:                fine work helped us get started. We thank the City of New York for assistance with
```
 In example 2, I used grep -i to find and print sentence that contains "New York". 

 [Third Example]
 ```
seosonghee@seosonghuis-MacBook-Air docsearch % grep -i "NSA-National Security Agency" technical/911report/*.txt  
technical/911report/chapter-13.2.txt:                Defense Sector; NSA-National Security Agency; NSC-National Security Council;
```
In the document in technical, it seems only one document which is chapter -13.2.txt only contains the word "NSA-National Security Agency".

I feel grep -i is useful when we want to find a word and see the contents of the word. I felt as grep-i ignore uppwer and lower case , grep - i can find more word and sentences related to the specific word.




