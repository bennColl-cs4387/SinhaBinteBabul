## Command Line History

````bash 
sinha@Sinha MINGW64 /c/repos/GIt murder mystery
$  ** git clone https://github.com/nivbend/gitstery.git** 
Cloning into 'gitstery'...
remote: Enumerating objects: 9481, done.
remote: Counting objects: 100% (9481/9481), done.
remote: Compressing objects: 100% (4560/4560), done.
remote: Total 9481 (delta 2627), reused 9479 (delta 2627), pack-reused 0 (from 0)
Receiving objects: 100% (9481/9481), 2.76 MiB | 4.86 MiB/s, done.
Resolving deltas: 100% (2627/2627), done.

sinha@Sinha MINGW64 /c/repos/GIt murder mystery
$ **cd gitstery/** 

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (master)
$ **ls**
_config.yml  instructions.txt  README.md  residents.txt

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (master)
$ ** cat instructions.txt**
---------------------------------------------------------------------------------------
A murder had been committed in Git Town!

The detective, Kyle Pumbinner, said the crime scene report is on the `gtpd-archive` branch. He
doesn't really remember the report ID... But he knows it was the first report he submitted after his
son's ninth birthday (which was Saturday, July 20th), and it was the only report he submitted that
week.

When you find a suspect, you'd probably want to interview them. To do that, first find out their
address. To go to that street, look for the street's name in the repository (Hint: it's a tag). To
go to house number N on that street, go to the Nth ancestor. If you'd like to inspect the
perimeters, you can look into the commit's contents - it'll contain a hash that you can view with
certain git commands.

Think you found the culprit? Check your answer with the following command:

echo "John Doe" | git hash-object --stdin | grep -iq -f /dev/stdin <(git show solution) && echo 'You found the murderer!' || echo 'No cigar, chief... Try again.'

Replace John Doe with the name of the suspect that you want to check.

For an extra challenge, try and solve the mystery without ever using `git checkout`.
---------------------------------------------------------------------------------------------------

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (master)
$ **git checkout gtpd-archive**
branch 'gtpd-archive' set up to track 'origin/gtpd-archive'.
Switched to a new branch 'gtpd-archive'

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (gtpd-archive)
$ **ls**
instructions.txt  README.md  residents.txt

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (gtpd-archive)
$ **git log**
commit ee35cc0590fd430baf738772f2d702c1bd7038c9 (HEAD -> gtpd-archive, origin/gtpd-archive)
Author: Ira Grazzitch <igrazzitch@gtpd.gittown.gov>
Date:   Mon Dec 30 22:12:00 2019 +0000

    Crime scene report #623616

    "My sister had told me some weeks before that I might have the pick of her geese for a Christmas
    present, and I knew that she was always as good as her word. I would take my goose now, and in it I
    would carry my stone to Kilburn. There was a little shed in the yard, and behind this I drove one of
    the birds--a fine big one, white, with a barred tail. I caught it, and prying its bill open, I
    thrust the stone down its throat as far as my finger could reach. The bird gave a gulp, and I felt
    the stone pass along its gullet and down into its crop. But the creature flapped and struggled, and
    out came my sister to know what was the matter. As I turned to speak to her the brute broke loose
    and fluttered off among the others.

    "'Whatever were you doing with that bird, Jem?' says she.

commit 66c44fb4114a2368cb966f523fd9726bad8f8ec0
Author: Angus Wunnard <awunnard@gtpd.gittown.gov>
Date:   Wed Dec 25 14:09:00 2019 +0000

    Crime scene report #361772

    "Your Majesty must pay. It must be bought."

    "She will not sell."

    "Stolen, then."

    "Five attempts have been made. Twice burglars in my pay ransacked her house. Once we diverted her
    luggage when she travelled. Twice she has been waylaid. There has been no result."

commit c09dbff971cb3bd1376d344eceea58638779913a
Author: Cybil Dopest <cdopest@gtpd.gittown.gov>
Date:   Sun Dec 22 19:42:00 2019 +0000

    Crime scene report #350977

    "Your own little income," he asked, "does it come out of the business?"

    "Oh, no, sir. It is quite separate and was left me by my uncle Ned in Auckland. It is in New Zealand
    stock, paying 4½ per cent. Two thousand five hundred pounds was the amount, but I can only touch the
    interest."

commit 77b67f5565400b1bab2fc6d594abe0e1bc55649f
Author: Cybil Dopest <cdopest@gtpd.gittown.gov>
Date:   Sun Dec 22 16:01:00 2019 +0000

    Crime scene report #152868

    "As you both locked your doors at night, your rooms were unapproachable from that side. Now, would
    you have the kindness to go into your room and bar your shutters?"

    Miss Stoner did so, and Holmes, after a careful examination through the open window, endeavoured in
    every way to force the shutter open, but without success. There was no slit through which a knife
    could be passed to raise the bar. Then with his lens he tested the hinges, but they were of solid
    iron, built firmly into the massive masonry. "Hum!" said he, scratching his chin in some perplexity,
    "my theory certainly presents some difficulties. No one could pass these shutters if they were
    bolted. Well, we shall see if the inside throws any light upon the matter."

    A small side door led into the whitewashed corridor from which the three bedrooms opened. Holmes
    refused to examine the third chamber, so we passed at once to the second, that in which Miss Stoner
    was now sleeping, and in which her sister had met with her fate. It was a homely little room, with a
    low ceiling and a gaping fireplace, after the fashion of old country-houses. A brown chest of
    drawers stood in one corner, a narrow white-counterpaned bed in another, and a dressing-table on the
    left-hand side of the window. These articles, with two small wicker-work chairs, made up all the
    furniture in the room save for a square of Wilton carpet in the centre. The boards round and the


sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (gtpd-archive)
$ **git log --reverse**
commit 908ca6a49d54bbc44dbbfa8195da2206ef8128a5
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    Git Town

commit 9655e409efe8b135231d2b03da27fc3f7c389b85
Author: Francine Wronchusher <fwronchusher@gtpd.gittown.gov>
Date:   Tue Jan 1 21:45:00 2019 +0000

    Crime scene report #82019

    "I do not wish to make a mystery," said he, laughing. "The matter was perfectly simple. You, of
    course, saw that everyone in the street was an accomplice. They were all engaged for the evening."

    "I guessed as much."

    "Then, when the row broke out, I had a little moist red paint in the palm of my hand. I rushed
    forward, fell down, clapped my hand to my face, and became a piteous spectacle. It is an old trick."

    "That also I could fathom."

commit 923eaec569541642da7dde03f11d0d6ae7d54ba3
Author: Ira Grazzitch <igrazzitch@gtpd.gittown.gov>
Date:   Thu Jan 3 08:37:00 2019 +0000

    Crime scene report #643126

    "I cannot tell."

    The banker wrung his hands. "I shall never see them again!" he cried. "And my son? You give me
    hopes?"

commit bf5b1fe921e82c8ad00cb8d089272a53b698d842
Author: Ira Grazzitch <igrazzitch@gtpd.gittown.gov>
Date:   Sat Jan 5 11:34:00 2019 +0000

    Crime scene report #214102

    "The fish that you have tattooed immediately above your right wrist could only have been done in
    China. I have made a small study of tattoo marks and have even contributed to the literature of the
    subject. That trick of staining the fishes' scales of a delicate pink is quite peculiar to China.
    When, in addition, I see a Chinese coin hanging from your watch-chain, the matter becomes even more
    simple."

    Mr. Jabez Wilson laughed heavily. "Well, I never!" said he. "I thought at first that you had done
    something clever, but I see that there was nothing in it, after all."

    "I begin to think, Watson," said Holmes, "that I make a mistake in explaining. 'Omne ignotum pro


sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (gtpd-archive)
$ **git log --after="2019-07-01" --before="2019-08-01"**
commit 31d22264bff278394ac54768f1662a6d5a21b375
Author: Aldo Chornoost <achornoost@gtpd.gittown.gov>
Date:   Wed Jul 31 21:02:00 2019 +0000

    Crime scene report #139024

    "Well, down they came to the west country, there was no shaking them off, and there they have lived
    rent free on my best land ever since. There was no rest for me, no peace, no forgetfulness; turn
    where I would, there was his cunning, grinning face at my elbow. It grew worse as Alice grew up, for
    he soon saw I was more afraid of her knowing my past than of the police. Whatever he wanted he must
    have, and whatever it was I gave him without question, land, money, houses, until at last he asked a
    thing which I could not give. He asked for Alice.

    "His son, you see, had grown up, and so had my girl, and as I was known to be in weak health, it
    seemed a fine stroke to him that his lad should step into the whole property. But there I was firm.
    I would not have his cursed stock mixed with mine; not that I had any dislike to the lad, but his
    blood was in him, and that was enough. I stood firm. McCarthy threatened. I braved him to do his
    worst. We were to meet at the pool midway between our houses to talk it over.

    "When I went down there I found him talking with his son, so I smoked a cigar and waited behind a
    tree until he should be alone. But as I listened to his talk all that was black and bitter in me
    seemed to come uppermost. He was urging his son to marry my daughter with as little regard for what
    she might think as if she were a slut from off the streets. It drove me mad to think that I and all
    that I held most dear should be in the power of such a man as this. Could I not snap the bond? I was
    already a dying and a desperate man. Though clear of mind and fairly strong of limb, I knew that my
    own fate was sealed. But my memory and my girl! Both could be saved if I could but silence that foul
    tongue. I did it, Mr. Holmes. I would do it again. Deeply as I have sinned, I have led a life of
    martyrdom to atone for it. But that my girl should be entangled in the same meshes which held me was
    more than I could suffer. I struck him down with no more compunction than if he had been some foul
    and venomous beast. His cry brought back his son; but I had gained the cover of the wood, though I
    was forced to go back to fetch the cloak which I had dropped in my flight. That is the true story,
    gentlemen, of all that occurred."

    "Well, it is not for me to judge you," said Holmes as the old man signed the statement which had
    been drawn out. "I pray that we may never be exposed to such a temptation."

    "I pray not, sir. And what do you intend to do?"

    "In view of your health, nothing. You are yourself aware that you will soon have to answer for your
    deed at a higher court than the Assizes. I will keep your confession, and if McCarthy is condemned I
    shall be forced to use it. If not, it shall never be seen by mortal eye; and your secret, whether
    you be alive or dead, shall be safe with us."

commit 92b165f2bf896b0f400d19b23528a5cb31cbbb3a
Author: Aldo Chornoost <achornoost@gtpd.gittown.gov>
Date:   Wed Jul 31 20:32:00 2019 +0000

    Crime scene report #975080

    "Your beer should be excellent if it is as good as your geese," said he.

    "My geese!" The man seemed surprised.

    "Yes. I was speaking only half an hour ago to Mr. Henry Baker, who was a member of your goose club."

    "Ah! yes, I see. But you see, sir, them's not our geese."

    "Indeed! Whose, then?"

    "Well, I got the two dozen from a salesman in Covent Garden."

commit 6093e1c111ac964ade7b6cca8b4d4068c76f34dc
Author: Angus Wunnard <awunnard@gtpd.gittown.gov>
Date:   Mon Jul 29 18:53:00 2019 +0000

    Crime scene report #317137

    "The glass still keeps very high," he remarked as he sat down. "It is of importance that it should
    not rain before we are able to go over the ground. On the other hand, a man should be at his very
    best and keenest for such nice work as that, and I did not wish to do it when fagged by a long
    journey. I have seen young McCarthy."

    "And what did you learn from him?"

    "Nothing."

    "Could he throw no light?"

    "None at all. I was inclined to think at one time that he knew who had done it and was screening him
    or her, but I am convinced now that he is as puzzled as everyone else. He is not a very quick-witted
    youth, though comely to look at and, I should think, sound at heart."

    "I cannot admire his taste," I remarked, "if it is indeed a fact that he was averse to a marriage
    with so charming a young lady as this Miss Turner."

commit 467d37e7086e724bf10b399a663c48d5f6950b6d
Author: Angus Wunnard <awunnard@gtpd.gittown.gov>
Date:   Thu Jul 25 08:09:00 2019 +0000

    Crime scene report #191558

    We got off, paid our fare, and the trap rattled back on its way to Leatherhead.

    "I thought it as well," said Holmes as we climbed the stile, "that this fellow should think we had
    come here as architects, or on some definite business. It may stop his gossip. Good-afternoon, Miss
    Stoner. You see that we have been as good as our word."

    Our client of the morning had hurried forward to meet us with a face which spoke her joy. "I have
    been waiting so eagerly for you," she cried, shaking hands with us warmly. "All has turned out
    splendidly. Dr. Roylott has gone to town, and it is unlikely that he will be back before evening."

    "We have had the pleasure of making the doctor's acquaintance," said Holmes, and in a few words he
    sketched out what had occurred. Miss Stoner turned white to the lips as she listened.

    "Good heavens!" she cried, "he has followed me, then."

    "So it appears."

commit 34433b62e6abb29f57b0089d0eda1e6004ff7ef3
Author: Aldo Chornoost <achornoost@gtpd.gittown.gov>
Date:   Wed Jul 24 22:07:00 2019 +0000

    Crime scene report #392309

    "'I quite follow you,' said I. 'The only point which I could not quite understand was what use you
    could make of a hydraulic press in excavating fuller's-earth, which, as I understand, is dug out
    like gravel from a pit.'

    "'Ah!' said he carelessly, 'we have our own process. We compress the earth into bricks, so as to
    remove them without revealing what they are. But that is a mere detail. I have taken you fully into
    my confidence now, Mr. Hatherley, and I have shown you how I trust you.' He rose as he spoke. 'I
    shall expect you, then, at Eyford at 11.15.'

    "'I shall certainly be there.'

    "'And not a word to a soul.' He looked at me with a last long, questioning gaze, and then, pressing
    my hand in a cold, dank grasp, he hurried from the room.

    "Well, when I came to think it all over in cool blood I was very much astonished, as you may both
    think, at this sudden commission which had been intrusted to me. On the one hand, of course, I was
    glad, for the fee was at least tenfold what I should have asked had I set a price upon my own
    services, and it was possible that this order might lead to other ones. On the other hand, the face
    and manner of my patron had made an unpleasant impression upon me, and I could not think that his
    explanation of the fuller's-earth was sufficient to explain the necessity for my coming at midnight,
    and his extreme anxiety lest I should tell anyone of my errand. However, I threw all fears to the
    winds, ate a hearty supper, drove to Paddington, and started off, having obeyed to the letter the
    injunction as to holding my tongue.

    "At Reading I had to change not only my carriage but my station. However, I was in time for the last
    train to Eyford, and I reached the little dim-lit station after eleven o'clock. I was the only
    passenger who got out there, and there was no one upon the platform save a single sleepy porter with
    a lantern. As I passed out through the wicket gate, however, I found my acquaintance of the morning
    waiting in the shadow upon the other side. Without a word he grasped my arm and hurried me into a
    carriage, the door of which was standing open. He drew up the windows on either side, tapped on the
    wood-work, and away we went as fast as the horse could go."

commit 0e63b5b41dec7b308fce23b5bc2676b4300312f2
Author: Kyle Pumbinner <kpumbinner@gtpd.gittown.gov>
Date:   Wed Jul 24 21:44:00 2019 +0000

    Crime scene report #956171

    Murder took place ten days ago, on July 14th. Coroner report says it was some time between 16:13 and
    19:37.

    According to the security guard that sat at the entrance to the factory, on the day of the murder no
    one came through the front door. So that leaves the back door, which requires an RFID card to open.

    With the help of the factory's IT department I managed to cherry-pick the relevant commits from the
    access log for all the electronically locked facilities on premise. They're on my personal
    'detectives/kpumbinner' branch. But they said the program doesn't have a search button... I'll have
    to sift through it to find who used "BACKDOOR_332". I put the log file in the evidence folder to
    look through later.

commit 8b95e8e569a46696653b06e4d10602c3339d5df0
Author: Cybil Dopest <cdopest@gtpd.gittown.gov>
Date:   Mon Jul 22 11:57:00 2019 +0000

    Crime scene report #319411

    "Oh, that! I thought of the salt that I have been working upon. There was never any mystery in the
    matter, though, as I said yesterday, some of the details are of interest. The only drawback is that
    there is no law, I fear, that can touch the scoundrel."

    "Who was he, then, and what was his object in deserting Miss Sutherland?"

    The question was hardly out of my mouth, and Holmes had not yet opened his lips to reply, when we
    heard a heavy footfall in the passage and a tap at the door.

    "This is the girl's stepfather, Mr. James Windibank," said Holmes. "He has written to me to say that
    he would be here at six. Come in!"

commit 2569d0444edc8ae4963ea4e5f093aa749ef9b5e4
Author: Ira Grazzitch <igrazzitch@gtpd.gittown.gov>
Date:   Fri Jul 19 21:36:00 2019 +0000

    Crime scene report #122979

    "'I had £4 a month in my last place with Colonel Spence Munro.'

    "'Oh, tut, tut! sweating--rank sweating!' he cried, throwing his fat hands out into the air like a
    man who is in a boiling passion. 'How could anyone offer so pitiful a sum to a lady with such
    attractions and accomplishments?'

    "'My accomplishments, sir, may be less than you imagine,' said I. 'A little French, a little German,
    music, and drawing--'

    "'Tut, tut!' he cried. 'This is all quite beside the question. The point is, have you or have you
    not the bearing and deportment of a lady? There it is in a nutshell. If you have not, you are not
    fitted for the rearing of a child who may some day play a considerable part in the history of the
    country. But if you have why, then, how could any gentleman ask you to condescend to accept anything
    under the three figures? Your salary with me, madam, would commence at £100 a year.'

    "You may imagine, Mr. Holmes, that to me, destitute as I was, such an offer seemed almost too good
    to be true. The gentleman, however, seeing perhaps the look of incredulity upon my face, opened a
    pocket-book and took out a note.

    "'It is also my custom,' said he, smiling in the most pleasant fashion until his eyes were just two
    little shining slits amid the white creases of his face, 'to advance to my young ladies half their
    salary beforehand, so that they may meet any little expenses of their journey and their wardrobe.'

commit 8f68ef494d0615b627b24a957cc72fcbf37c781a
Author: Cybil Dopest <cdopest@gtpd.gittown.gov>
Date:   Sat Jul 13 09:42:00 2019 +0000

    Crime scene report #433038

    "But not more so than I to find you."

    "I came to find a friend."

    "And I to find an enemy."

commit 9a8e71b787b70d80df86b7f8940dca8f9b97c1cf
Author: Angus Wunnard <awunnard@gtpd.gittown.gov>
Date:   Fri Jul 12 21:47:00 2019 +0000

    Crime scene report #139439

    "Which of you is Holmes?" asked this apparition.

    "My name, sir; but you have the advantage of me," said my companion quietly.

    "I am Dr. Grimesby Roylott, of Stoke Moran."

commit cf772f73ab834f0b0066e2e2b12b6cc4217739b6
Author: Kyle Pumbinner <kpumbinner@gtpd.gittown.gov>
Date:   Thu Jul 11 16:27:00 2019 +0000

----------------------------------------------------------------------------------------

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (gtpd-archive)
$ **git checkout detectives/kpumbinner**
branch 'detectives/kpumbinner' set up to track 'origin/detectives/kpumbinner'.
Switched to a new branch 'detectives/kpumbinner'

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (detectives/kpumbinner)
$ **ls**
evidence/  instructions.txt  README.md  residents.txt

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (detectives/kpumbinner)
$ **cd evidence/**

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **ls**
access.log

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **cat access.log**
SECURITY_ROOM_1
BACK_ROOM_231
CABINET_67_C1
PRINTER_ROOM_76
GARAGE_2
GARAGE_2
BACK_ROOM_231
SECURITY_ROOM_1
BACK_ROOM_231
GARAGE_2
PRINTER_ROOM_76
SECURITY_ROOM_1
PRINTER_ROOM_76
BACK_ROOM_231
BACK_ROOM_231
BACK_ROOM_231
SECURITY_ROOM_1
SECURITY_ROOM_1
BACKDOOR_332
MAIN_FREEZER
GARAGE_2
BACK_ROOM_231
GARAGE_1
GARAGE_1
SECURITY_ROOM_1
SECURITY_ROOM_1
PRINTER_ROOM_76
PRINTER_ROOM_76
GARAGE_2
SECURITY_ROOM_1
CABINET_34_A
GARAGE_2
CABINET_67_C1
CABINET_34_A
CABINET_67_C1
BACKDOOR_332
SECURITY_ROOM_2
SECURITY_ROOM_1
SECURITY_ROOM_2
GARAGE_1
GARAGE_2
CABINET_34_A
CABINET_67_C1
BACKDOOR_332
BACK_ROOM_231
CABINET_67_C1
CABINET_34_A
MAIN_FREEZER
PRINTER_ROOM_76
GARAGE_1
PRINTER_ROOM_76
GARAGE_2
GARAGE_1
MAIN_FREEZER
GARAGE_1
SECURITY_ROOM_1
SECURITY_ROOM_2
CABINET_34_A
CABINET_67_C1
CABINET_67_C1
--------------------------------------------------------------------------------------------------------

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **git blame access.log**
e693164d (Bruno Proizzan     2019-07-14 08:31:00 +0000  1) SECURITY_ROOM_1
1c8cde18 (Ives Printiddle    2019-07-14 08:44:00 +0000  2) BACK_ROOM_231
1e95c300 (Bruno Proizzan     2019-07-14 08:46:00 +0000  3) CABINET_67_C1
026a3787 (Elvira Pommass     2019-07-14 08:57:00 +0000  4) PRINTER_ROOM_76
840266ba (Sybil Glorp        2019-07-14 09:02:00 +0000  5) GARAGE_2
16fcb259 (Ives Printiddle    2019-07-14 09:35:00 +0000  6) GARAGE_2
434a1174 (Kevin Hethork      2019-07-14 09:39:00 +0000  7) BACK_ROOM_231
b26a9ecd (Sterling Brammer   2019-07-14 09:51:00 +0000  8) SECURITY_ROOM_1
9a61eda5 (Elvira Pommass     2019-07-14 10:01:00 +0000  9) BACK_ROOM_231
3aa89c5c (Bruno Proizzan     2019-07-14 10:17:00 +0000 10) GARAGE_2
0bc8d662 (Kevin Hethork      2019-07-14 10:31:00 +0000 11) PRINTER_ROOM_76
88fc757f (Sterling Brammer   2019-07-14 10:34:00 +0000 12) SECURITY_ROOM_1
c7c25ca3 (Kingsley Cotold    2019-07-14 10:46:00 +0000 13) PRINTER_ROOM_76
0b2cf417 (Bruno Proizzan     2019-07-14 10:58:00 +0000 14) BACK_ROOM_231
d5ba13f0 (Bruno Proizzan     2019-07-14 11:01:00 +0000 15) BACK_ROOM_231
bba0dcc2 (Kevin Hethork      2019-07-14 11:12:00 +0000 16) BACK_ROOM_231
e5e48ae1 (Francine Worrupper 2019-07-14 11:18:00 +0000 17) SECURITY_ROOM_1
22c932c8 (Sterling Brammer   2019-07-14 11:37:00 +0000 18) SECURITY_ROOM_1
d9289fe4 (Lyndon Huskupper   2019-07-14 12:06:00 +0000 19) BACKDOOR_332
20da2c2b (Elvira Pommass     2019-07-14 12:14:00 +0000 20) MAIN_FREEZER
9032c193 (Kevin Hethork      2019-07-14 12:18:00 +0000 21) GARAGE_2
95ec8be5 (Bruno Proizzan     2019-07-14 12:20:00 +0000 22) BACK_ROOM_231
2da53454 (Elvira Pommass     2019-07-14 12:22:00 +0000 23) GARAGE_1
949b6a24 (Kingsley Cotold    2019-07-14 12:25:00 +0000 24) GARAGE_1
539b293b (Bruno Proizzan     2019-07-14 12:30:00 +0000 25) SECURITY_ROOM_1
dff1b3a4 (Bruno Proizzan     2019-07-14 12:35:00 +0000 26) SECURITY_ROOM_1
b27e76f5 (Elvira Pommass     2019-07-14 12:54:00 +0000 27) PRINTER_ROOM_76
1fe911db (Bruno Proizzan     2019-07-14 13:26:00 +0000 28) PRINTER_ROOM_76
c11935d5 (Sybil Glorp        2019-07-14 13:30:00 +0000 29) GARAGE_2
6645bd55 (Francine Worrupper 2019-07-14 13:43:00 +0000 30) SECURITY_ROOM_1
cd5f8ea9 (Kingsley Cotold    2019-07-14 13:46:00 +0000 31) CABINET_34_A
127902a9 (Elvira Pommass     2019-07-14 13:47:00 +0000 32) GARAGE_2
a63076bf (Sybil Glorp        2019-07-14 13:51:00 +0000 33) CABINET_67_C1
7cfcc4c9 (Elvira Pommass     2019-07-14 14:07:00 +0000 34) CABINET_34_A
552e081e (Elvira Pommass     2019-07-14 14:10:00 +0000 35) CABINET_67_C1
09d0547f (Cosmo Siwkonk      2019-07-14 14:16:00 +0000 36) BACKDOOR_332
a8e490a8 (Sybil Glorp        2019-07-14 14:29:00 +0000 37) SECURITY_ROOM_2
d484e5b1 (Bruno Proizzan     2019-07-14 14:56:00 +0000 38) SECURITY_ROOM_1
ef5e66f0 (Bruno Proizzan     2019-07-14 14:57:00 +0000 39) SECURITY_ROOM_2
5bad5971 (Kevin Hethork      2019-07-14 14:58:00 +0000 40) GARAGE_1
91a95dc2 (Francine Worrupper 2019-07-14 15:02:00 +0000 41) GARAGE_2
b77d02e3 (Bruno Proizzan     2019-07-14 15:11:00 +0000 42) CABINET_34_A
ce7f2227 (Ives Printiddle    2019-07-14 15:20:00 +0000 43) CABINET_67_C1
13611d85 (Brock Stuickard    2019-07-14 15:23:00 +0000 44) BACKDOOR_332
728bb449 (Elvira Pommass     2019-07-14 15:30:00 +0000 45) BACK_ROOM_231
2bdb2193 (Sybil Glorp        2019-07-14 15:30:00 +0000 46) CABINET_67_C1
5b96ff20 (Ives Printiddle    2019-07-14 15:49:00 +0000 47) CABINET_34_A
17d1e75b (Kevin Hethork      2019-07-14 16:14:00 +0000 48) MAIN_FREEZER
c9983ccf (Sybil Glorp        2019-07-14 16:16:00 +0000 49) PRINTER_ROOM_76
e224f2b5 (Francine Worrupper 2019-07-14 16:28:00 +0000 50) GARAGE_1
23f2f971 (Kingsley Cotold    2019-07-14 16:32:00 +0000 51) PRINTER_ROOM_76
ba176115 (Sybil Glorp        2019-07-14 16:35:00 +0000 52) GARAGE_2
a0d83a11 (Sybil Glorp        2019-07-14 16:39:00 +0000 53) GARAGE_1
e839ffb7 (Elvira Pommass     2019-07-14 16:44:00 +0000 54) MAIN_FREEZER
24dace60 (Bruno Proizzan     2019-07-14 17:04:00 +0000 55) GARAGE_1
e21ce2e8 (Sybil Glorp        2019-07-14 17:06:00 +0000 56) SECURITY_ROOM_1
40fa72a5 (Francine Worrupper 2019-07-14 17:06:00 +0000 57) SECURITY_ROOM_2
23dbcfa6 (Elvira Pommass     2019-07-14 17:13:00 +0000 58) CABINET_34_A
bd57df06 (Ives Printiddle    2019-07-14 17:33:00 +0000 59) CABINET_67_C1
333028ee (Sybil Glorp        2019-07-14 17:49:00 +0000 60) CABINET_67_C1
------------------------------------------------------------------------------------------------------------

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **grep "BACKDOOR 332" access.log**

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **grep "BACKDOOR_332" access.log**
BACKDOOR_332
BACKDOOR_332
BACKDOOR_332

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **git blame access.log | grep "BACKDOOR_332" access.log**
BACKDOOR_332
BACKDOOR_332
BACKDOOR_332

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **git blame access.log | grep "BACKDOOR_332"**
d9289fe4 (Lyndon Huskupper   2019-07-14 12:06:00 +0000 19) BACKDOOR_332
09d0547f (Cosmo Siwkonk      2019-07-14 14:16:00 +0000 36) BACKDOOR_332
13611d85 (Brock Stuickard    2019-07-14 15:23:00 +0000 44) BACKDOOR_332

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **ls**
access.log

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery/evidence (detectives/kpumbinner)
$ **cd ..**

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (detectives/kpumbinner)
$ **ls**
evidence/  instructions.txt  README.md  residents.txt

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (detectives/kpumbinner)
$ **grep "Brock Stuickard" residents.txt**
Brock Stuickard 9 Beaconside

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (detectives/kpumbinner)
$ **grep "Cosmo Siwkonk" residents.txt**
Cosmo Siwkonk   26 Balcombe Close

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (detectives/kpumbinner)
$ **grep "Lyndon Huskupper" residents.txt**
Lyndon Huskupper        73 Tamworth Drive

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery (detectives/kpumbinner)
$ **git tag**
solution
street/badgers_dene
street/balcombe_close
street/beaconside
street/bowler_street
street/cliff_place
street/corbet_close
street/down_close
street/glan_road
street/glendale
street/harvey_street
street/holmefield_avenue
street/larch_walk
street/moor_end
street/sunningdale_drive
street/tamworth_drive
street/valentia_road
street/ventnor_terrace
street/wantage_close
street/wellswood_gardens
street/wilson_gardens
--------------------------------------------------------------------------------------------------------

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/balcombe_close))
$ **git checkout street/beaconside**
Previous HEAD position was f36a4e6 Balcombe Close
HEAD is now at 5e37024 Beaconside

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/beaconside))
$ git log -n 10
commit 5e37024660b27211f54c09121d152ac519baa0ce (HEAD, tag: street/beaconside)
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    Beaconside

commit b04c9eb9bde711c00515fa9fa9e86fadbd86c0eb
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    1 Beaconside

    "He looked inside the envelope. 'So it is,' he cried. 'Here are the very letters. But what is this
    written above them?'

    "'Put the papers on the sundial,' I read, peeping over his shoulder.

    "'What papers? What sundial?' he asked.

    "'The sundial in the garden. There is no other,' said I; 'but the papers must be those that are
    destroyed.'

    "'Pooh!' said he, gripping hard at his courage. 'We are in a civilised land here, and we can't have
    tomfoolery of this kind. Where does the thing come from?'

    "'From Dundee,' I answered, glancing at the postmark.

commit aa1fb5ed03cc9aa1afef830ad7bc41a4ff083e38
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    2 Beaconside

    "At Reading I had to change not only my carriage but my station. However, I was in time for the last
    train to Eyford, and I reached the little dim-lit station after eleven o'clock. I was the only
    passenger who got out there, and there was no one upon the platform save a single sleepy porter with
    a lantern. As I passed out through the wicket gate, however, I found my acquaintance of the morning
    waiting in the shadow upon the other side. Without a word he grasped my arm and hurried me into a
    carriage, the door of which was standing open. He drew up the windows on either side, tapped on the
    wood-work, and away we went as fast as the horse could go."

    "One horse?" interjected Holmes.

    "Yes, only one."

    "Did you observe the colour?"

    "Yes, I saw it by the side-lights when I was stepping into the carriage. It was a chestnut."

commit de58095ae7bd21b39fbb10f834156477ace0a78d
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    3 Beaconside

    "And Irene Adler?"

    "Threatens to send them the photograph. And she will do it. I know that she will do it. You do not
    know her, but she has a soul of steel. She has the face of the most beautiful of women, and the mind
    of the most resolute of men. Rather than I should marry another woman, there are no lengths to which
    she would not go--none."

    "You are sure that she has not sent it yet?"

    "I am sure."

    "And why?"

    "Because she has said that she would send it on the day when the betrothal was publicly proclaimed.
    That will be next Monday."

commit 3456743d5a7c6907f4f1ab6d2e38d4dfe81e5ad8
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    4 Beaconside

    "From Hatherley Farm-house to the Boscombe Pool is a quarter of a mile, and two people saw him as he
    passed over this ground. One was an old woman, whose name is not mentioned, and the other was
    William Crowder, a game-keeper in the employ of Mr. Turner. Both these witnesses depose that Mr.
    McCarthy was walking alone. The game-keeper adds that within a few minutes of his seeing Mr.
    McCarthy pass he had seen his son, Mr. James McCarthy, going the same way with a gun under his arm.
    To the best of his belief, the father was actually in sight at the time, and the son was following
    him. He thought no more of the matter until he heard in the evening of the tragedy that had
    occurred.

    "The two McCarthys were seen after the time when William Crowder, the game-keeper, lost sight of
    them. The Boscombe Pool is thickly wooded round, with just a fringe of grass and of reeds round the
    edge. A girl of fourteen, Patience Moran, who is the daughter of the lodge-keeper of the Boscombe
    Valley estate, was in one of the woods picking flowers. She states that while she was there she saw,
    at the border of the wood and close by the lake, Mr. McCarthy and his son, and that they appeared to
    be having a violent quarrel. She heard Mr. McCarthy the elder using very strong language to his son,
    and she saw the latter raise up his hand as if to strike his father. She was so frightened by their
    violence that she ran away and told her mother when she reached home that she had left the two
    McCarthys quarrelling near Boscombe Pool, and that she was afraid that they were going to fight. She
    had hardly said the words when young Mr. McCarthy came running up to the lodge to say that he had
    found his father dead in the wood, and to ask for the help of the lodge-keeper. He was much excited,
    without either his gun or his hat, and his right hand and sleeve were observed to be stained with
    fresh blood. On following him they found the dead body stretched out upon the grass beside the pool.
    The head had been beaten in by repeated blows of some heavy and blunt weapon. The injuries were such
    as might very well have been inflicted by the butt-end of his son's gun, which was found lying on
    the grass within a few paces of the body. Under these circumstances the young man was instantly
    arrested, and a verdict of 'wilful murder' having been returned at the inquest on Tuesday, he was on
    Wednesday brought before the magistrates at Ross, who have referred the case to the next Assizes.
    Those are the main facts of the case as they came out before the coroner and the police-court."

    "I could hardly imagine a more damning case," I remarked. "If ever circumstantial evidence pointed
    to a criminal it does so here."

    "Circumstantial evidence is a very tricky thing," answered Holmes thoughtfully. "It may seem to
    point very straight to one thing, but if you shift your own point of view a little, you may find it
    pointing in an equally uncompromising manner to something entirely different. It must be confessed,
    however, that the case looks exceedingly grave against the young man, and it is very possible that
    he is indeed the culprit. There are several people in the neighbourhood, however, and among them
    Miss Turner, the daughter of the neighbouring landowner, who believe in his innocence, and who have
    retained Lestrade, whom you may recollect in connection with the Study in Scarlet, to work out the
    case in his interest. Lestrade, being rather puzzled, has referred the case to me, and hence it is
    that two middle-aged gentlemen are flying westward at fifty miles an hour instead of quietly
    digesting their breakfasts at home."

    "I am afraid," said I, "that the facts are so obvious that you will find little credit to be gained
    out of this case."

    "There is nothing more deceptive than an obvious fact," he answered, laughing. "Besides, we may
    chance to hit upon some other obvious facts which may have been by no means obvious to Mr. Lestrade.
    You know me too well to think that I am boasting when I say that I shall either confirm or destroy
    his theory by means which he is quite incapable of employing, or even of understanding. To take the
    first example to hand, I very clearly perceive that in your bedroom the window is upon the right-
    hand side, and yet I question whether Mr. Lestrade would have noted even so self-evident a thing as
    that."

commit 442586607a46b30e7bfc275fa718d1ed5db64e13
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    5 Beaconside

    "That is not quite so common, is it? Ah, me! it's a wicked world, and when a clever man turns his
    brains to crime it is the worst of all. I think that I have seen enough now, Miss Stoner, and with
    your permission we shall walk out upon the lawn."

    I had never seen my friend's face so grim or his brow so dark as it was when we turned from the
    scene of this investigation. We had walked several times up and down the lawn, neither Miss Stoner
    nor myself liking to break in upon his thoughts before he roused himself from his reverie.

    "It is very essential, Miss Stoner," said he, "that you should absolutely follow my advice in every
    respect."

    "I shall most certainly do so."

    "The matter is too serious for any hesitation. Your life may depend upon your compliance."

    "I assure you that I am in your hands."

commit 6627764f2ccaa6cb5bea2ccfddee3c80d141ac04
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    6 Beaconside

    "What!" Sherlock Holmes staggered back, white with chagrin and surprise. "Do you mean that she has
    left England?"

    "Never to return."

commit ce911e405ccb078a14f1a2d734507122870f9a37
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    7 Beaconside

    "But have you," I asked, "formed any definite conception as to what these perils are?"

    "There can be no question as to their nature," he answered.

    "Then what are they? Who is this K. K. K., and why does he pursue this unhappy family?"

commit 89e5cfcbedd52af9d56238853af3a6380f5e86cc
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    8 Beaconside

    "That is enough." She rose briskly from her chair with the anxiety all swept from her face. "I shall
    go down to Hampshire quite easy in my mind now. I shall write to Mr. Rucastle at once, sacrifice my
    poor hair to-night, and start for Winchester to-morrow." With a few grateful words to Holmes she
    bade us both good-night and bustled off upon her way.

    "At least," said I as we heard her quick, firm steps descending the stairs, "she seems to be a young
    lady who is very well able to take care of herself."

    "And she would need to be," said Holmes gravely. "I am much mistaken if we do not hear from her
    before many days are past."

commit 92f6e05c6aa06c791f402d7e19649fa1f0ec76c6
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    9 Beaconside

    Yeah, of course I used the backdoor to the factory, that's the closest entrance to the freezer and I
    brought in some ingrediants that can't really stand the heat.

    At the time of the murder I was at a block party right down the street from here, we threw the party
    for one of the neighbors who got back from the hospital after an accident. I was with my kids. You
    can ask anyone who's been there.

    Oh wait, you know what? We took a picture... Let me get my phone.

    See? That's me, that's the neighbor, here's my little girl. And you see the timestamp?

    So yeah, I really don't have anything to do with that... Barely knew the victim...

    But you know what? I did see someone rushing out of the factory... He got into a green Hyundai, you
    don't see many of those around here... Probably a rental. I didn't catch his face, was just weird
    seeing someone running off like that... Come to think about it, maybe that person had something to
    do with it?

    Anyways, best of luck catching whoever did it!
--------------------------------------------------------------------------------------------------------

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/beaconside))
$ **git checkout street/balcombe_close**
Previous HEAD position was 5e37024 Beaconside
HEAD is now at f36a4e6 Balcombe Close

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/balcombe_close))
$ **git log --skip 26**
commit bc6870d8093a33d9a69acc94a1cda16ee2d7195d
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    26 Balcombe Close

    No one's home...

    You can take a look around though.

commit 77d19b1a916b206582ecb6979b84659d9beafc5f
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    27 Balcombe Close

    The station-master laughed heartily. "No, sir, Dr. Becher is an Englishman, and there isn't a man in
    the parish who has a better-lined waistcoat. But he has a gentleman staying with him, a patient, as
    I understand, who is a foreigner, and he looks as if a little good Berkshire beef would do him no
    harm."

    The station-master had not finished his speech before we were all hastening in the direction of the
    fire. The road topped a low hill, and there was a great widespread whitewashed building in front of
    us, spouting fire at every chink and window, while in the garden in front three fire-engines were
    vainly striving to keep the flames under.

    "That's it!" cried Hatherley, in intense excitement. "There is the gravel-drive, and there are the
    rose-bushes where I lay. That second window is the one that I jumped from."

commit 658ba902940210c6017748efd3ebdb63f6e10270

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/balcombe_close))
$ **git show bc6870d8093a33d9a69acc94a1cda16ee2d7195d**
commit bc6870d8093a33d9a69acc94a1cda16ee2d7195d
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    26 Balcombe Close

    No one's home...

    You can take a look around though.

diff --git a/investigate b/investigate
index 96b6a70..18d6cc8 100644
--- a/investigate
+++ b/investigate
@@ -1 +1 @@
-a847106689850c8e841882b910c1e5d67c6ec8b6
\ No newline at end of file
+c8411c73e49372dbdb644beef2ea841b403fc476
\ No newline at end of file

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/balcombe_close))
$ **git show c8411c73e49372dbdb644beef2ea841b403fc476**
Nobody's home. From the stack of letters in the mailbox nobody's been here for a good few days.

Without a warrant you can't get into the house, but you can still checkout the area. Maybe talk with
some of the neighbors.

The guy next door says he barely ever spoke to the suspect, "was a bit of a loner" is what he says.
Doesn't know what type of vehicle he drives.

You take a stroll around the house, there's a back porch that probably seen better days. You spot a
driveway next to it leading to a garage. The door's open and you see a green Hyundai parked there.

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/balcombe_close))
$ **git tag**
solution
street/badgers_dene
street/balcombe_close
street/beaconside
street/bowler_street
street/cliff_place
street/corbet_close
street/down_close
street/glan_road
street/glendale
street/harvey_street
street/holmefield_avenue
street/larch_walk
street/moor_end
street/sunningdale_drive
street/tamworth_drive
street/valentia_road
street/ventnor_terrace
street/wantage_close
street/wellswood_gardens
street/wilson_gardens

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/balcombe_close))
$ **git checkout street/tamworth_drive**
Previous HEAD position was f36a4e6 Balcombe Close
HEAD is now at 72c01a9 Tamworth Drive

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/tamworth_drive))
$ **git log --skip 72**
commit b87b4b754cc882eb453973a2b23a33231c677450
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    72 Tamworth Drive

    "Yes, they have shown extraordinary energy. The whole garden has already been minutely examined."

    "Now, my dear sir," said Holmes. "is it not obvious to you now that this matter really strikes very
    much deeper than either you or the police were at first inclined to think? It appeared to you to be
    a simple case; to me it seems exceedingly complex. Consider what is involved by your theory. You
    suppose that your son came down from his bed, went, at great risk, to your dressing-room, opened
    your bureau, took out your coronet, broke off by main force a small portion of it, went off to some
    other place, concealed three gems out of the thirty-nine, with such skill that nobody can find them,
    and then returned with the other thirty-six into the room in which he exposed himself to the
    greatest danger of being discovered. I ask you now, is such a theory tenable?"

    "But what other is there?" cried the banker with a gesture of despair. "If his motives were
    innocent, why does he not explain them?"

    "It is our task to find that out," replied Holmes; "so now, if you please, Mr. Holder, we will set
    off for Streatham together, and devote an hour to glancing a little more closely into details."

commit f8a5b218b1eaee3b111ae5ef536f919e8d3afca2
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    73 Tamworth Drive

    No one's home...

    Maybe take a look around the perimeter?

commit 26500f63364cc0036a94465aa7df529337f1c5dc
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    74 Tamworth Drive

    "I really don't know what to say. I have a fairly long list at present."

-------------------------------------------------------------------------------------------
sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/tamworth_drive))
$ **git show f8a5b218b1eaee3b111ae5ef536f919e8d3afca2**
commit f8a5b218b1eaee3b111ae5ef536f919e8d3afca2
Author: Dolores Wholfump <mayor@gittown.gov>
Date:   Tue Jan 1 00:00:00 2019 +0000

    73 Tamworth Drive

    No one's home...

    Maybe take a look around the perimeter?

diff --git a/investigate b/investigate
index 7240a04..2121ca5 100644
--- a/investigate
+++ b/investigate
@@ -1 +1 @@
-7abc61f1a2519635488c2a4c9881b8a67f8896ae
\ No newline at end of file
+22f733298423b814f1da31bee3e0063c72ed6e71
\ No newline at end of file

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/tamworth_drive))
$ **git show 22f733298423b814f1da31bee3e0063c72ed6e71**
There's no one answering the door. Obviously you won't break in because you don't have a warrant or
anything. But nothing's wrong with looking around the place...

You check around the house, there's no car. Not even a driveway. You do find a bike resting against
the fence. It's pretty close to the factory, so makes sense the suspect bikes to work.

Just to make sure, you ask some of the neighbors, they confirm that the suspect doesn't own a car.
One of them says he doesn't even have a license.

Another neighbor says he saw the suspect coming back from work on the day of the murder at about
5PM, they chatted for a bit before his sister picked him up to visit their parents. They live pretty
far away, so that places him away from Git Town at the time of the murder.
------------------------------------------------------------------------------------------------------------------------------
sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/tamworth_drive))
$ **echo "Cosmo Siwkonk" | git hash-object --stdin | grep -iq -f /dev/stdin <(git show solution) && echo 'You found the murderer!' || echo 'No cigar, chief... Try again.'**
You found the murderer!

sinha@Sinha MINGW64 /c/repos/GIt murder mystery/gitstery ((street/tamworth_drive))
$ cd ..

sinha@Sinha MINGW64 /c/repos/GIt murder mystery
$  history > history_for_print.txt

