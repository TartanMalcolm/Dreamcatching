Here's the transcript: 

---

0:01
okay so from my side I want to present a um angle or reasoning
0:08
around removing back chat from being a
0:14
thing like um this thing uh I'm assuming that uh on the
0:20
right hand side I don't need to see any of that text Cu illegible uh that was the State Board yeah yeah no that's fine
0:27
but there's there's nothing specific in text doesn't matter it's the layout that's the thing and so back chat used
0:33
to pop up as a it would [Music]
0:42
um wait on back chat would do this right it
0:48
would come and go
0:54
yeah what yeah that is sloppy isn't it um
1:02
[ __ ] happen you uh what what are you doing there oh no it's G again this is
1:07
the slide it's it does this on purpose to show what happens okay so all right
1:12
okay right the user is using the thing back chat slides in back chat slides out all that now there's um two concepts
1:21
that I want to talk about number one is the user experience of what on Earth
1:26
happens if um I'm in this thread and then I want to
1:32
start talking to the CRM mhm and then and then I want to come back to
1:39
this thread so that's you know I don't think that I
1:45
should blank This Thread I think what I should do is let
1:51
you switch to this the CRM thread has to be
1:58
running in the CR repo it can't be in your repo because it needs to run under
2:04
the control of the application that's running it mhm right like it's got all
2:09
the Bots and all that and it can access parts of the repo that you yourself can't access but the thread can
2:14
communicate with it and all that a bunch of DRS and a bunch and then you also need to be able to let the owners of
2:21
that repo app see what everyone's done so you they need to see all the threads
2:27
of all the staff plus the staff need to see the threads too so that people can
2:32
see what's going on who did this why did they do that but you don't want to see
2:37
all their private chats that they were having all the other stuff and nor do
2:43
you want to make it so that when they're playing around in their own environment
2:49
and they call in a sketchy agent that's borderline
2:55
legit if it had access to all the data in the thread and the the thread contained all the CRM interactions then
3:02
you've now leaked the company info so you can't have that either and
3:08
so what I thought of doing is having the notion of a
3:16
um it's a thread it's sectioned threads and so it's sort of colorcoded or or
3:24
showing in the UI that somehow this portion of the message history
3:30
it belongs to belongs to this other
3:37
location so that when you're when you're in the enclosing
3:43
one uh I'm sorry I need to draw a picture I'm no I think you think going
3:51
from okay yeah yeah okay so you're like
3:56
message message message and this is you in your private space and then you
4:01
go hey I want to connect to the CRM and the system goes hokey doie and then your
4:08
messages show in a maybe a different color or just a different way to indicate that this portion is separate
4:17
from this portion and then somewhere down here you go hey I want to get out of here I want to go back to where I was
4:23
before and then it goes okay and you come back to this thread right right right right so you got layers but but
4:29
also um tricky part is uh for the blue stuff when you're doing let's call it
4:36
Agent X yeah um and uh so if you add in a few more blue layers underneath the
4:42
black at the bottom when Agent X is uh talking it's thread it's only the blue correct and
4:51
then when you're talking to agent black it's only the black that's right and now
4:56
blue doesn't need to see black for any reason well it it shouldn't
5:03
because no no no no yeah I knew this was I knew this was contentious but this is
5:09
my conclusion is that blue blue has no business knowing about
5:16
black whatsoever uh in this instance yes yeah
5:21
well in any instance because black is the parent and blue is the
5:27
child um yes but the uh uh suby here or I think you probably
5:32
already thought about this uh subtlty is CRM might have um uh sub Bots inside of
5:39
that correct we should have different colors and you they would the Bots would change but
5:45
the thread would stay the same so like your your CRM thread in the the black lines the Bots
5:52
are switching in and out but they're your Bots with access to your data in the blue thread the Bots are switching
5:59
in and out but it's only the crm's data okay it's all right okay so let's
6:05
think about this um if you add in another color let's make it a bit more pruy um I in um a pink layer now is who
6:13
is who is who is pink a child of is pink a child of black or pink a child of blue
6:19
uh well let's see black is how right yeah black is the original you started and here you are and how's your friend
6:26
yep yeah um and then you've gone and done blue with CRM yeah then you gone
6:32
let's say back to Hal yeah um and then you're now in pink so I went back to how
6:38
and then I went I don't have a pink Red's going to have to do you I love that you wanted that color most of all
6:45
but anyway so oh sorry salmon salmon inside inside of a Sal inside of a
6:50
salmon the salmon internal internal Swatch hell um okay and then so that's
6:58
the the other thing like
7:04
uh maybe that's Bank just make it make it sort of seem important so now you've
7:11
got um three threads going um now I
7:17
assume um well does black know about the
7:22
whole Shang I think that black I think that black knows about the whole shebang
7:29
but black black cannot see inside it so black would get like a summary of what
7:34
happened so that when you're in Black you're like hey remember when I was talking to the CRM and I said blah blah
7:40
blah blah blah um what what was that about again so that you
7:46
can uh no that's the um well given your uh emphasis on uh
7:53
leakage uh what you'd want to do is um black uh doesn't know anything about
8:00
I think that I think that like it's okay for black to see completely inside the
8:05
CRM the thing that's not okay is for black to switch to an agent that isn't
8:12
trusted and then also allow full visibility into the thread so another
8:18
way that we could the second one of I absolutely agree with yeah the second way we could have handle this is to say
8:25
that black is special in that it's only certified safe Bots and in which case it would be okay
8:33
to let black see the whole thread
8:39
verbatim yeah because if if the user saw the thread then it's okay for the user's
8:44
agent to see the thread so long as the agent is trusted another way of doing it
8:50
possibly is um black knows that you've been talking to you know this hussy CRM
8:57
B yeah yeah um and as soon as you ask about a question about the CRM bot
9:03
you're you're now talking uh to the CRM bot so there's a difference between thread and display
9:10
right we can display it yeah I just didn't want to I just didn't want to
9:15
um end up in a position where I'm showing the user one thing and then the
9:21
user tries to talk about it or select it because I want to make the messages
9:27
selectable like so I can pick this one and talk about
9:33
it well the question is who you talking to so say if for example CRM had its
9:41
own uh long thread it's version of how how CM yeah yeah that's right um and so
9:49
uh all your um your black uh how just knows right you're talking about the CRM
9:56
now I'm just going to pass you to the CRM now the question is would you ever
10:01
want to um have any kind of conversation about uh red and blue while talking to
10:09
Black it's like black blue it's not it's sort of yes yes you might you might
10:16
because if we're going to present them all together then of course at some
10:22
point someone will want to have a multi-threaded conversation now the other option is
10:28
to uh switch out the whole thread so that when you talk to the CRM it's a
10:33
blank thread and you're just only seeing that data right and then when you switch
10:39
back do as essentially a new H it looks like a new H yeah only is only on they
10:45
can do all those yeah yeah yeah and so we would indicate to you using a lozenge
10:50
of some kind that um which which what the location of your thread
10:58
was so for example that little lozen there might change to to help tell you
11:04
where where you are like are you talking to your H or are you talking to the
11:10
CRM um all those kinds of things right so really is just an
11:15
interesting one okay so uh I love my analogy so here's an analogy right you've got
11:22
uh uh the user is a double agent talking to uh the Soviets and NATO at the same
11:28
time right uh you don't want you want the uh the user in this
11:36
case the double agent to be able to do that you don't want nle ever to know anything about the Soviets you don't
11:42
want the Soviets ever to know anything about correct okay well it sounds pretty
11:48
obvious then that what you're advocating for is that when I whenever I switch
11:55
threads the whole display resets it sounds like it it sounds like when
12:01
when you um call up the CRM then you get a new how okay now the the thing we
12:07
could add to that possibly is allow uh so we were talking about um the top
12:13
level black uh how yeah knows that you're talking to the CRM just doesn't know what you're talking
12:19
about um it could it it could and maybe it should but I think that um if we
12:28
separ at the visual presentation it makes
12:34
it so that you can't be talking to
12:40
red and you can't talk to Red about blue or you can't talk to Red about black but
12:47
you can talk to black about red and blue yeah but here's here's the thing right so you're in black and you've been
12:54
talking black knows you've been talking to blue and red yeah um you ask a
12:59
question in Black uh that is actually the business of
13:05
blue um and it passes on the question to this the uh blue and the blue can decide
13:10
whether to answer or not it's like so you want that that's the like the knowledge Realms of each black says all
13:19
red says only red blue says only blue uh no no uh if you were to uh so let me let
13:26
me think through this so and this is probably not right but that's go be so you're in
13:32
Black uh talk to Blue talk to black talk to Red talk to black okay then black
13:38
he's saying right uh blue is um generated this file I went red to know
13:46
about it uh should be able to ask blue but blue has its own permissions blue no
13:54
no no no black isn't black
14:00
has the power like all all the conversations with blue actually under
14:05
the hood go through black because black is the users terminal thread and so it's
14:12
it's like if you SSH into another terminal even though you're securely
14:19
connected and this thing's got permissions up the wazu all your keystrokes are still going through your
14:25
original terminal to get there yeah um yeah uh that's quite good anation so so
14:31
if I want to do the file transfer what I would do is I would have to say uh black
14:36
reach into blue and grab me this file and it would be like okay cuz I've got the history and then once I've got it I
14:44
would oh that's R the wrong way but you know what I mean and then I'd put it into red right you've now got some weird
14:51
kind of character here it looks like it's crying yeah it is that's how I feel every day working with these problems I
14:58
would I I would um uh I would add a bit onto that uh in that narrative uh black
15:06
uh says blue you've got this file I've just been told you got this file give me
15:11
the file blue should be able to under it own permission say no you're not getting that file well yeah yeah yeah yeah
15:19
absolutely but if you
15:26
hadn't yes um but that's no different to being in blue
15:34
and you you wouldn't have access to that file anyway anything that anything that
15:40
blue lets you access black therefore has access to but of all the files in the
15:47
CRM your thread within the CRM may be denied access to some because of who
15:53
black is because black is your identity and you converse with the CRM as black
15:59
within the black thread and that's why if if the CRM thread lets you see a file
16:06
black can see that file so it's a bit like having uh two servers and laptop
16:12
and uh two servers individually have their own permissions correct but your laptop has permissions to into both yeah
16:20
yeah so I do an SCP on one yep now got it yeah and it would come but it would
16:25
have to come through your laptop to the other server right and so the permissions um are uh if you were to try
16:33
and SCP a file which um blue didn't allow you to have a black yeah going say
16:39
you get to that yeah yeah that's right yeah that makes and then Additionally
16:44
you may the system may allow red and blue to
16:49
communicate independently of black anyway so you know that that's allowed
16:56
too I just want to make that point yeah yeah um well that would be uh blue and
17:02
red would uh inherit the permissions of black saying can you guys can we talk
17:09
it's like yeah yeah we can talk oh right so like um black could give them permission to talk to each other on
17:15
behalf of black right because ultimately black has the permissions of the user is
17:20
correct effectively is the the user yep okay awesome okay so that settles that then
17:27
we will when you when you dial in when you first start up you get the black
17:33
thread which is your how and then you say I want to work on the CRM and it
17:39
does the login and all that stuff and then it resets the message thread
17:45
because you're looking at uh a dedicated new thread that's running over here on the
17:51
CRM yep but all your messages are still going through black under the hood they
17:57
just don't show up as um they don't show up in the message
18:02
history of black because you're now talking to this new dedicated thread yeah now when you thr up when new thread
18:09
uh and in blue for example um and then red uh you don't want is accidental
18:16
leakage um so every all the information is in Black by the fact that you can access blue and red that means you have
18:23
permissions correct um so is there any way that
18:29
information could leak between blue and red in that situation not exp not at all yeah so um the other
18:37
thing is that um I want to switch I want to remove
18:45
back chat from being a thread to being
18:51
an agent within hell and so I think that I still want to have the
19:00
Summoner um and I'll try and draw a picture here because when I've explained
19:06
this to you in the past and then I listened to my explanation I was unimpressed so the message all
19:14
messages under the hood come into black in terms of like this is
19:21
your uh your terminal where it comes in by messages do you mean prompts prompts yeah from
19:28
the user saying anything first goes to here then it's going to go to
19:35
the I think it goes to the Summoner where it says
19:43
um draw the Summoner in green and the Summoner says did the user want to keep talking
19:51
to the thread that they're in or did they want to jump out and talk to the
19:56
containing thread or some other thread in the stack so I want to int the cont
20:03
switch right yeah I want to introduce the concept of a stack and a a thread stack is like I could be say I'm in red
20:11
and then I I cause the Summoner to get me out of here like I'm like help please
20:18
help I want to stop talking to the bank I they want to take my house and then
20:24
the Summoner intercepts it doesn't send it to the bank drops you back to black
20:30
because that's the most appropriate thread that it thought you wanted to be in right
20:36
then you go I want to talk to this other thread which is the orange thread don't
20:42
know what it does maybe it does juice cuz it's lunchtime then when you're in the orange thread you
20:49
say I want to talk to the salmon thread but that's now you didn't go oh what the
20:58
fluff let see what you're saying right here we go the purple pimper nickel and then it
21:06
goes to this other thread but this the stack has
21:12
gone um oh dear oh dear my artistic expression is
21:19
lacking um goes there and in this case the stack still contains orange and then
21:27
it contains pimp in the because
21:32
the when I when I hit the Summoner and I'm like oh Summoner get me out of
21:37
here um it knows the thread stack because let's say this was called
21:45
the the juice bar and this was called the the allergens bot cuz I was going to
21:52
order a fancy sort of a smoothie but I was like it's got monk fruit in it I've
21:57
never heard of that in my illus to it it be me yeah yeah and then I could go H
22:03
Summoner get me I could go summon I want to talk about holidays and holiday and
22:08
summon is like oh that's okay I'm going to drop you back to hell because that's got nothing to do
22:14
with anything on the stack that sounds a lot like backat though but hang
22:20
on it's it never back chat used to have some functionality the Summoner is only
22:28
for switching you between threads now the Summoner used to switch you between
22:36
either back chat or the current thread Now it only chooses
22:41
between which threads are currently open before there were only over two threads
22:46
open now I'm saying we could have it could be stacked arbitrarily deep and suon it can switch you between
22:54
them right mhm okay and and and and
23:00
history it's just sounds like a top level switch board yes but it doesn't switch between
23:07
agents it switches between
23:12
threads ah yes and so I could I could be down
23:20
here talking about monk fruit allergies and I could say oh wait I want to go I
23:25
want to go talk to the bank again and then summon a would drop you back
23:30
into this thread here right so uh to pick up analogy from
23:37
our last call um I was talking about uh you've got a very large seat and
23:43
mahogany desk and one laptop and different number of people we can call on yeah and uh I'm working on this oh
23:50
get yourself in here do that right go away next yeah uh or go away and you
23:57
figure it out and come back okay so that is um one um pattern mhm the second
24:03
pattern is uh I've got an infinite uh office and I'm walking around with uh no
24:11
no I'm going into each office and there's a new laptop each time yeah that
24:18
was our that was like several models ago for us yeah so that's interesting so
24:23
we've got so that seems to be um well those those two models um
24:31
seem to make sense right right but working on one thing or am I working on
24:36
yeah yeah but so so originally we were walking around to each office right right then then we modified
24:45
that to say um we want to switch the office uh sorry we want to
24:52
switch the worker we want to stay in one office and we want to switch out the workers and now what I'm saying is that
24:58
we want to be in one office switch out the workers and then switch office and
25:03
then switch out workers there and then switch office again so it's like those two things
25:09
combined yeah yeah yeah exactly or um it's uh one extends the other because uh
25:15
being able to switch offices um reduces you back to ignoring the previous office
25:22
yeah state right but but the difference being that these
25:27
offices can act as um conceptual isolation barriers but
25:33
primarily they would act as permissions barriers so when you're like when you go
25:40
to the bank the bank will switch out agents in front of you based on your
25:45
request but you're at the bank it's not you're at the juice bar the juice bar agent would never appear behind the
25:52
counter at the bank the bank would switch out its agent right yeah yeah you're going for like a you know
26:00
want the guy behind the desk saying yeah ah would you like a lawn like yeah yeah yeah but when I'm but when I'm talking
26:06
to when I'm talking to the juice bar I should be able to pull in some info from
26:11
a chat that I had with the bank um and I should be able to haul
26:17
that in somehow well uh let's go with that analogy so the juice bar guy you're
26:23
getting your juice from uh it says uh this juice uh cost about
26:29
uh you know I don't have $1,000 um would you like a loan it's like well talk to
26:35
my bank the juice guy calls the bank and the bank guy either says I can't that's
26:41
yeah that's different that's that's independent of you that's got nothing to do with your frame of reference that's
26:48
happening behind the scenes that's right but um there's no real difference between the user and Bot or than that's
26:56
uh there is there is because the the if the juice bar rang up the bank the bank would probably be like who the who the
27:02
fluff are you I don't know no there but the only difference is permissions right the juice bar phones up the bank says
27:07
I'm not telling you that yeah and then you hand the phone and it's like yeah yeah yeah I've going through all the identification thing it's like oh yeah
27:14
you hand the you hand the phone over yeah it's sort of like that so I don't know I don't know how to do
27:22
that um it's almost it's almost like you want to call the Summoner or chat and be
27:29
like hey can you pull in that info from that other chat and then drop it in here
27:35
but then that starts to make backchat be a dedicated thread
27:44
again you know you kind of want to be like uh drop me out you you kind of want
27:50
to make it two moves like you're in the juice bar you go Summoner drop me back
27:55
drop me back to hell then in how you're like uh grab the info from the bank okay
28:01
and then you're like okay uh take that with me into the juice
28:07
bar yeah but the two moves um I mean why aren't there extra moves life it's like
28:14
uh [ __ ] that's an expensive smoothie right let me call a bank right Bank yeah
28:19
but that would be a context switch for you you're in you're in the Smoothie Bar you'd you'd halt your interaction with
28:25
the Smoothie Bar and you'd communicate with the Bank somehow you wouldn't get
28:30
the Smoothie Bar to call the bank for you the Smoothie Bar doesn't actually inter yeah the Smoothie Bar doesn't know
28:36
who your bank they also don't want to deal with it they don't make any they're like what the [ __ ] dude call my bank
28:42
it's like you call your yeah you call your bank I'm not i' got smoothies to make you know yeah um okay so that's
28:50
that's the uh the kind of can I can I can I chart that up as a a bit of a kink
28:56
that I don't know how to Sol it but we'll just play with it I still don't understand yes uh so I'm happy with this
29:03
one but I still don't I get why we need to kill backchat because backchat is
29:09
back becomes an a special thread that interacts with artifact right well
29:16
backchat was a special thread that was the highest level thread because it
29:21
could navigate you around through different threads and now what I'm saying is that there's only
29:28
this this black thread takes on the role of what back chat used to be and so you
29:35
never actually you you know you never actually relieve it why not if suar is basically
29:44
the one who um understands the context switch the thread switch a thread switch
29:50
is not a context switch it's it's bigger uh no the third switch is the result the
29:55
contest uh switch is be trigger well no you can have contact switches inside a
30:02
thread like within the CRM it's a contact switch to go from routing to bank reconciliation to truck maintenance
30:09
to you right that's context switching too yeah but um what I'm saying is no the um threat switch is okay we're going
30:16
to do this now but uh the Summoner something needs to say um okay so you
30:24
just said take me to you know this yourm yeah let make it simple yeah um now the
30:31
tech me to the CRM needs to be interpreted by a bot correct um and that is a context
30:37
switch previously talking about Ro and Josh now I'm talking about CRM Su goes context switch right
30:43
gotcha okay what you want is this right I think that the Summoner then
30:50
um exists on this top level thread so that you when you're like why did you
30:58
put me in this spot it would actually be a conversation
31:04
in the top level because the top level would show why it you could drill down into
31:11
why it switched you to whichever thread it did and you could see in your chat
31:17
history your thread switches and then when you go click on them or talk about
31:22
them it'll take you to that thread in a way yep y yeah with that sounds a lot
31:30
like sorry bit yet um if
31:36
I excuse me excuse me with what I'm about to
31:43
doing by if I do that and now this is now totally independent but I replace it
31:51
with some sort of a special looking message
31:59
if I that would indicate you know uh switch to CRM
32:06
thread when I click on that select it or otherwise tell using my voice that I
32:13
want to talk about that thread yeah it will show the message history of that
32:20
thread in the stateboard yes how's that yes that's
32:26
good right yeah yeah yeah yeah exactly so so it'll make a widget that'll be
32:31
specially it'll be unmistakable that you're looking at a windowed view right
32:37
it's like now I'm talking to my bank it's like it's like this is a window into the conversation of the bank but
32:44
you are not talking to the bank at this point you're just looking at what you said to the bank exactly and you've got
32:50
like a notebook of everything you said to the bank you got a notebook everything said to the just bar I was
32:56
like right okay going to the Bank notebook here uh the bank knows nothing
33:01
about the juice bar juice bar knows nothing about the bank um how as your autor ego yeah knows
33:08
that you got two notebooks and Sumer sounds a lot like a
33:13
like a so that's um okay that mechanism there is how you
33:18
could do the um transferring information from your bank conversation to your
33:24
juice conversation because you would select the bank conversation while you're in
33:30
Hell or yeah while you're in hell you would select the bank conversation and then you would say um bring the bank
33:38
balance info over to my juice conversation and the Summoner or the switchboard or whatever it's become now
33:46
would know that it would first of all have that data and then it would know that you want to now go into right right
33:53
which sounds a lot like a credit card transaction right when you sweap your card to the juice bar uh the juice bar
34:00
knows nothing about your bank right uh it goes off and uh goes through whatever
34:06
you know Swift or whatever Network and all it comes back with is yes go for it
34:11
doesn't know anything else but all the juice wants to know is do you have $1,000 to pay for right yeah right okay
34:18
okay okay y so in that scenario you're treating the credit card as a piece of information that's authorized by the
34:24
bank that proves to the juice bar that exactly but the justar had for example
34:31
um uh asked the bank uh give me all your personal information of this guy and
34:38
they go no [ __ ] off not doing that just come back with no you don't
34:43
get okay all right so to recap you're only ever able to see one
34:50
thread at a time when you switch to a remote thread like a conversation with
34:56
the CRM or or with the bank um that looks like a whole new
35:02
thread to you there's a stack of threads that is uh handled
35:10
by it's not the switchboard it's the the thing that switches you between
35:18
threads um that that will always interpret your messages and determine
35:24
whether or not you were talking to the Summoner itself or some other thread and
35:29
it will always toggle you around between those and the Summoner actions happen on
35:35
your base thread which is this original how the black it sounds about right so
35:41
name it for me what's the what's the Summoner name well before we go into the naming thing uh let me get this right
35:47
because we've got two modes of operation here isn't it it's like um uh uh I've only ever talked to Black
35:56
in this thread um now I want to talk to CRM right that was a switchboard thing
36:03
so now no that's not a switchboard the switchboard as we had defined it before was switching between agents in the same
36:11
thread right so who does that switch it's like I haven't talked to that's
36:16
what I'm asking you to name it's I had called it the Summoner because the Summoner the Summoner
36:22
handled determining whether you were talking to back chat the thread or the current thread that you're focused on so
36:30
the Summoner is the one who invokes and instantiates new thread that you haven't
36:35
talked to before correct okay the instantiator were kind of cool
36:44
uh we give it a pistol well it might not be it it might it might send you
36:52
to a an instantiator agent because how
36:58
you instantiate a new remote thread would be different for the CRM as it
37:03
would be for the bank so it might be a convoluted process and the Summoner
37:09
can't possibly know that process in advance but it could know how to send
37:14
you to an agent that could figure that out for you H okay I've got an idea uh what's what's the name with the uh the
37:21
top level I think Judy Den last time in the Bond films she was the one who's like sending agents it's like do this
37:31
m so that's is that M yeah yeah but it's not you're not
37:37
switching between agents you're switching
37:43
between whole groups of Agents like MI6 CIA talk to the CIA talk to the
37:51
Bolivian government right right exactly and there's a whole bunch of stuff underneath that and there's a local agent okay well m m works for me buddy
37:59
I'm cool with that that's a that's a novel way to describe it interesting enough we also get for free Q for the
38:05
tools but anyway uh might be a bit too
38:11
much okay we we'll save that for
38:16
later um m
38:23
m extra large
38:29
so okay all right so now a message comes in
38:37
from the user a a piece of text comes in from the users hitting enter in the keyboard it
38:45
comes into the backend terminal this is like the this is not an AI agent this is mechanical it's pass the
38:52
authentication yeah this artifact level artifact then passes it to its first AI
38:58
interaction which is with the agent M Agent M is special and that m is m is an
39:07
agent that runs on the base thread but M gets everything
39:14
first and then m is aware of all of the threads that are
39:21
currently uh that have been active mhm
39:27
um with some window and then depending on how M interprets that you
39:37
will you will be your page you will change and you will end up
39:44
in a different thread right does m uh save all those threads we've got one in
39:51
I don't know is China whatever does m get to say right we need to go to to uh
39:58
buen we haven't talked to buen yet what happens at that point that
40:05
would drop you back to the base thread which is
40:11
how and then how would use the switchboard to
40:16
pick the appropriate agent to do what you wanted who's talking so m is talking to
40:23
how no M does not talk M only Rel days okay so um IM switches how is how
40:32
does how know about when is AR how doesn't but how has the agents that it
40:38
uses when it doesn't know things so m is a right we've got four well let's go
40:46
with this analogy because it's quite fun we got four operations going and five this doesn't five because you've always
40:52
got home base so m is based at MI6 and these other threads are like the
40:58
CIA MI5 CIA um all these different things yeah and now um M uh gets a
41:08
request in saying we don't have any uh operations going at the moment covers
41:13
this and it says how create me a new create this guy a new operation in
41:20
Planet series one more time please so um uh in
41:26
the analogy so uh M gets a request in looks through right we've got something
41:31
in Moscow Tel Aviv Beijing and Washington y we don't have anything in W
41:38
are yep uh so um M then says we don't
41:44
have anything in Ben throw up an operation in Ben no M
41:50
says Hey hell over to you all right so I can't do
41:56
this you do M says we have no active operations based on this request how
42:03
sort it out right right and and how uh diligent dude that he is goes to right
42:09
switchboard get me when series wherever the MI6 yeah get me the search function
42:16
uh get me the web browsing function get me all these other things and then how works with the user to figure out what
42:22
the user meant right and then now we''ve uh see we now I've got an operation in
42:28
vaner that thread and goes oh brilliant I've got an extra operation here
42:35
yeah okay all rights to work okay um
42:41
could be a little bit jarring on the viewer though cuz if I'm
42:46
if I'm looking at this thread um if I'm looking at one thread and then I get switched over to
42:54
something else this screen going to just sort of drop away and then this new
43:00
screen's going to pop up with this new thread is that
43:05
okay should be okay right it is quite Jing I don't until we use it just like
43:12
yeah we'll have to why don't we just see right cuz logically it makes sense yeah I don't want to have other widgets like
43:20
listing your threads so you can manually select them thumnails yeah right it's like that we
43:26
failed at that point um so like it it should be a big deal to
43:31
switch operations because you shouldn't be dancing between them all the time you
43:37
know like when you use the CRM you're [ __ ] you're using the CRM right now
43:42
you can tell how to use the CRM on your behalf right so I think
43:50
that's different be chatting to the CRM directly is very different to talking to
43:57
and saying Hell you know how we're logged into the CRM I want you
44:02
to use this bot that I just made to do all my work today go that's different
44:08
that's you're still you're still talking to hell at that point but there's
44:13
interactions happening with the CRM that could be populating the thread with the CRM too right but it's not how how is
44:21
how is uh special because how inherits the Privileges of the user yeah yeah is
44:27
the trusted the the sanctuary he's the inner sanctum of the user okay all right
44:33
now so that's cool we'll deal with that and then we'll just I think it's faster to just do it and then see how it feels
44:41
and then work with that okay so the next issue yeah sorry
44:48
sorry yeah as a general thing throw out there it's much better to get the logic
44:54
right because if the logic is right and it seems weird then that's training yeah
45:00
uh or gooey yeah the logic be right the logic is the most important thing and I
45:05
think if we just make the bare minimum interfaces for the logic so you're in
45:10
agreeance with using the M using M as the thread
45:16
switcher uh yes yep yes and then when you're in each thread they depending on
45:23
how the thread has been configured keeping in mind that it's the vendor's Choice how to configure that thread um
45:30
the thread may have a switchboard in place right and uh yeah uh just to uh do
45:38
some Crossfire on this one um are two analogies of I'm working on my laptop in
45:43
my uh office and I'm calling people in y That's a thread I'm moving to another
45:49
office in my infinite office yep to work on this other thing that's the switch board thing right right right and just
45:56
to understand that model you may you and I may go into the same office and look
46:01
at the same laptop and we both collaborate on putting things in agents are being switched in and out to do our
46:08
bidding and then I might be like got to go buddy and I go back to my office or some other office and carry on doing
46:15
what I was doing there right yeah okay and
46:20
finally I can also tell one of my agents in another office to act like me and
46:27
talk to that office where you're in and you you wouldn't know whether it
46:34
was genuine me or how acting on my behalf um well yes absolutely because uh
46:40
the way be thinking about it is the user and how how is aoxy for yeah they look the same right in the whole ballpark
46:48
they look the same okay so the next problem
46:54
is well it's not nearly maybe it's a feature um is the concept
47:05
of the concept of having a thread
47:13
finish so uh wow this just like
47:20
um let me try and let me if you just I I'll tell you a very different story
47:26
I'll tell you a very different story about something that's that's equally useful but not related at all and then
47:33
from that I hope I can show the problem okay so I made a thing that I
47:39
was trying to get ready for you because I thought you would like it and then I ran out of time um what I've done oh man
47:48
that's so sweet I think you I got you a cookie but I ate it um I copied your
47:56
meeting bot mhm I put it in as an
48:02
agent mhm I more or less copied it identically and then I gave it the YouTube fetch
48:08
function which allows it to oh man pull in
48:14
transcripts yeah um and I had as in a slide I hit an interesting bug that occu
48:19
this is why I didn't finish it because I spent all of uh yesterday dealing with this bug where our our YouTube session
48:27
previous to this one was Bloody long and when I did YouTube fetch the system
48:33
crashed artifact crashed because the
48:39
actions uh the way I'd built it because of limitations on the Deno KV store an
48:45
action can't be more than 65 kiloby because actions are supposed to
48:51
be regret that limit yeah no no that's not that's not true
48:57
I when I store binary data or files There's No Limit because I use a library
49:04
that breaks it up into 65k chunks okay but when I'm sending actions I don't do
49:12
that and it occurred to me look I can either break up the actions so that they can be unlimited size but the choice
49:20
that I've made that I want to run by you because it sounds contentious is I actually want to set the action limit it
49:27
quite low because what in this case what
49:33
should have done happened is that when YouTube fetch was called it should
49:40
have the isolate that was running should not have returned the transcript as a
49:48
reply to the request it should have written it to a file on artifact and
49:55
then sent back the path to the file seems because it doesn't know that's
50:00
doesn't know what you want to do with it no and so if you send it back what happens is it gets smacked straight into
50:07
context now a lot of the time you want to do that but uh it's not I don't think
50:13
it's a good pattern to do that by default because you've got no way like what if I what if the isolate wanted to
50:21
return 5 gabes well interesting enough uh I've been this uh the uh prompt by saying um
50:31
here's the file just say got it um and it doesn't go into the thread
50:38
all you get in the thread is got it right but then it's uh it remembers it and can recall it and retrieve it and so
50:44
on so yeah that makes sense to me that mirror is what I've been doing in uh in
50:51
prom land okay so anyway that was a bug I so so you're okay if I set that action
50:57
limit to be quite low because actions are supposed to be control instructions
51:04
they are not supposed to be payloads in in my opinion they're not meant to be
51:09
like binary data they're not meant to be big they're supposed to be instructions
51:15
and for that yeah if if I've got this right um yes I agree in that uh now the
51:22
size of instruction is something else but uh PE Lords being being dumped somewhere and then referenced back seems
51:30
absolutely sensible okay great all right well let's what I have done let me just check
51:39
that I [Music] um H where are we
51:48
YouTube I want to say trust me this is worth it but um I don't know if it runs
51:54
so it might not be worth it all right we roll family I I love a good far too
52:00
early test I really
52:12
do test tests sorry buddy I'm just going to oh
52:18
you switch yeah I know cuz I I only want to
52:24
run meeting bot
52:49
okay okay it's good wait wait wait wait it's just running tests hang on it's
52:57
gone and run oh cuz I got two ones my bad my bad sorry about that only only
53:02
only only you're the only one and so are you be only
53:08
one which is completely obviously not
53:23
right so we got this was the TPS
53:29
report it ran one iteration it completed one in the test cases there was only one
53:35
test case and it ran one it completed one and it had no success so it failed
53:44
but the prompts this was the prompt that went
53:49
in mhm and then it got back a whole lot of
53:54
output which would have been [Music]
54:06
oh it didn't read it [Music]
54:13
into uh where does it say the output
54:27
say it executed there it ran that with the
54:38
prompt and then it said give me the transcript oh I know what's happened
55:05
if if this is like dragging on too much you can definitely tell me but this is
55:10
this is my life this is what Su I'm cheting you're on here this is this is
55:16
this is my this is my life this is what I have to do
55:26
uh that's right so path was required
55:35
and in meeting bot I need to tell it to give a
55:47
path if you had to Fitch info from YouTube you
55:54
will need [Music] to choose a
56:00
suitable path to write the transcript
56:08
to such as YouTube
56:23
slash transcript underscore
56:29
video ID I think that was it cuz I changed it
56:38
to I had I had the YouTube isolate generating the file name but actually
56:45
it's better if the meeting bot calls the uh YouTube function with doesn't know
56:52
where what right yeah the meeting the meeting bot should choose the should
56:58
choose the name
57:05
yeah hopefully that worked but what oh
57:13
dear didn't work now that was an open AI
57:22
area oh I get those occasionally um quite often if you run it a few seconds
57:29
later don't know what those guys are messing around under the hood or traffic or
57:38
whatever that's weird yeah what these guys are doing
57:43
let's see if hopefully an upgrade yeah yeah these guys are messing around with the under the hood but
57:49
they're I think they're doing rapid like hourly updates or something like that
58:01
uh it still asked for the transcript why is it asking for the
58:07
transcript like it came back it called it as a drone and then its response
58:19
was um please give me the transcript for the video but I I had it working before
58:27
when the path was generated what did what did you put the point
58:33
um you just move it you need to pistol whip it a bit like transcript is oh if if you put in
58:43
if uh must always fetch a YouTube users
58:48
will provide you with a transcript of a meeting or a YouTube url to Fitch the transcript from or a video D for YouTube
58:56
video to F the transcript from okay that sounds reasonable right uh it does but I
59:02
think you need to piss the whip a bit tell me what to do okay so what you got you got two options uh we provide you
59:07
with the transcript um uh I assume that no transcript is
59:14
going to be provided and fetched from YouTube If no YouTube uh is available
59:20
then ask for a transcript
59:27
that doesn't seem right because it seems like uh the reason why I'm pushing back
59:33
on your is cuz this did work before the only difference is I've required it to
59:39
choose the path that's the only change well the way to test it is um don't give an option um
59:47
users will provide uh a URL so I think it's getting confused
59:55
because it doesn't know where whether you're giving you transcript or URL and it's going yeah which one is it you are
1:00:02
right you are right so can I try this and then if this doesn't work I'll try your thing yeah yeah
1:00:30
okay but what I liked about this was being able to test that whole thing by
1:00:36
just writing a markdown test file and going go like that's that I thought was
1:00:42
pretty sweet it's nice H so that did work it called the
1:00:50
thing but it um made it Absolut loot where it should
1:00:56
be relative oh right okay which is a reasonable mistake to make a
1:01:04
scoop and this is where I want to give you that ability to change the function
1:01:09
definitions cuz I'm just changing it here like I'm changing it in the the API
1:01:18
description which Alters The Prompt but I don't have a way to give you that at the moment so that's why I want to
1:01:24
change that format to to let you modify that as part of your prompting process
1:01:30
yeah cool well this is fun I feel like it's one way or another going to
1:01:42
work oh wait wait wait wait what was that
1:01:49
error path must be relative don't give me absolute path
1:01:56
you scumbag how do I bash it into be be nice
1:02:02
to it where are you talking about path relative path doesn't know what a relative path is um give it an example
1:02:08
okay must end in. Json and must start with DOT
1:02:15
slash how about that yeah be nice to it first time you've ever said
1:02:23
that in like the last year that we've been dealing with this [ __ ] I've never
1:02:28
heard that so this is your life right
1:02:34
twiddling around with the oh yeah yeah yeah yeah exactly it's uh win nice witer
1:02:39
pistol whop so we' we've definitely collided right like we're I'm doing your job and you're sort of doing mine yeah
1:02:47
oh there's an error there what was that error no no error where's where's the ah it uh the test fail if I use only
1:02:54
because there's like other tests that should have run two all right okay that's all so this was the output of the
1:03:01
test case um that was the prompt and it still scored to
1:03:07
zero um here's the reasoning
1:03:18
oh this is message was a request for the transcripts not defend for conclusion or
1:03:23
analysis of video okay so the output
1:03:33
was so it fited the
1:03:40
transcript and then it said oh please give me the trans [ __ ]
1:03:48
sake this is is this your life this is what this is what you hate okay oh yeah
1:03:53
yeah uh okay so it's saying please give me um why does it not think it's got the
1:03:59
trans I got it I got it once the function has returned use
1:04:06
the files read function to read the
1:04:12
transcript from the path you gave the
1:04:17
YouTube Fitch function it didn't know to read it back
1:04:25
in it definitely called The Fitch but it didn't know to read it back in so this
1:04:32
is like I'd imagine that this step that I'm doing here would be running in the
1:04:37
browser for you where it's the tests um kicking off after you've twiddled the bot yeah
1:04:46
yeah and you get closer and closer yeah cuz there's uh some Nuance active
1:04:53
voice really works right the users will provide you is a different
1:05:00
and a much weak much more weak way of saying you will be provided by for
1:05:07
example um it still came back and said please
1:05:14
give me the transcript I need to tell it to read from the path that it just
1:05:20
got okay you told up what the right okay so tell me through this so we it's
1:05:25
already fetch the path it knows what the path is so it gener it generated the path and then it called the fetch
1:05:31
function correctly um but then the function returns with just the
1:05:38
description so should I uh yeah yeah um so give it uh a process um count this is
1:05:45
Pudo code it's like um you will receive back X from X you to do
1:05:54
y for
1:06:31
doesn't know what a transcript is Ah that's a good
1:06:37
point you said you will receive oh that's a great Point that's a great point
1:07:20
you butt you you God damn it
1:07:31
a path for the YouTube F function to write the transcript
1:07:38
to.
1:07:44
Json you will receive back a title and a description of the
1:07:49
video uh but again you'll receive back a title and a description but no transcript like yeah
1:07:57
yeah
1:08:18
um how about that uh you still haven't told her what the transcript is okay
1:08:23
where would I do that um okay so uh users will provide you with a transcript
1:08:30
of a meeting you YouTube patch the transcript from
1:08:36
video uh if you have to patch the transcript from the YouTube use the YouTube petch function you must choose
1:08:43
path for the YouTube petch function to write the transcript to still haven't um
1:08:49
said so what did you get back from that YouTube fetch uh it's a text
1:08:56
uh a big long line of text that represents the transcribed version of the YouTube video so is it the actual
1:09:03
transcription or um some kind of pointer to the
1:09:09
transcription sorry uh so I I choose the path that I want to write the transcript
1:09:16
to I then call the fetch function with that path the fetch function writes to that
1:09:23
path and then when when I get back the the video title then I go read and get
1:09:30
it in uh okay I think what I've done wrong is that it's confusing it by what I
1:09:36
return from that function so why don't I just return um transcript downloaded and
1:09:42
then give it back the path and then it will be like oh that's pretty [ __ ] obvious what I do with that yeah sounds
1:09:48
like it should work okay this is this is frustrating and fun it is fun isn't it
1:09:56
and yeah it's a lot like training a dog
1:10:01
frustrating in a fun oh god look this is my
1:10:08
mistake at the top level description of the function this is what I said see he's trying he's trying his
1:10:17
best I know it's like you don't make sense like what do you mean I really want to please you what do you mean I a
1:10:24
little AI span was trying to get all this fetched fetched fetch yes yes yes yes no that's WR or right like
1:10:30
[Laughter] H you this will write the
1:10:41
transcription Json object to the given
1:10:46
path and [Music]
1:10:53
return the title and description of the
1:10:59
YouTube video oh God after matter yeah I think
1:11:05
so um except for the uh spelling of transcription but uh
1:11:11
yeah there's one mattera that uh realized is
1:11:16
uh um doing all this really really really requires a lot of
1:11:23
the human to actually be clear in yeah yeah and so making making a bot that
1:11:28
could look at all that and then tell you and be like uh it sort of seems like you
1:11:35
did something conflicting that's that's why I built how how three is like my my
1:11:40
uh thinking is too messy you tell me what I've missed yeah um and a similar
1:11:46
thing it easily be uh built um for this use case but it's
1:11:53
amazing how much you how W you um [ __ ] up as a human I
1:12:00
know one of my favorite ones we're talking about about one of my favorite ones is asking it say um what was asked
1:12:06
or implied but never answered get this meeting that you've been in for an hour and everyone's going
1:12:11
yeah yeah we know exactly what we're doing it's like Oh you talked about this and nobody said anything about it yeah someone asked this you never answered it
1:12:18
um it's quite revealing how [ __ ] we are we are so [ __ ] we yes what's the
1:12:24
funniest thing though is that we're so [ __ ] and unaware of it and so we don't think
1:12:31
we're [ __ ] and you don't actually not like that whole time I was just like oh this bot's [ __ ] stupid what's going
1:12:37
on but actually the my bad it always does something
1:12:42
reasonable I think this is yeah this The Humbling thing it does exactly what you say know what you
1:12:50
meant I'm going to get that my Tombstone I think what's that
1:12:56
you're going to get a B right do exactly what you said but not what you
1:13:15
meant okay and now I'm going to come back where I'm going to
1:13:21
return um success is going to be a
1:13:29
Boolean and then the path is going to
1:13:36
be the path to the saved transcription
1:13:52
file okay and now
1:14:02
I'm glad that you're seeing me struggle like this cuz this is how my whole [ __ ] day goes this is my whole day
1:14:10
but only recently has it become a bot prompting issue as well so that's sort of good that this is I'm I'm glad we're
1:14:17
we're finally mashing in the middle you know um your uh your syntax
1:14:23
and layout there I would be struggling with um but well as you can see I'm
1:14:29
struggling with the bot prompting so that's
1:14:35
good yes it did it this is the function call it was like it finally went files
1:14:41
read and then here's the path be nice to the bot and the bot will be nice to you
1:14:46
beest thou nicest to the bot and then what did it say and then it
1:14:53
still said please give me the transcript it's in there hold on why why
1:15:00
why um which uh in the in the flow here where is that um long for assistant
1:15:07
agents meeting MD please give me the transcript up here what was the thing that was
1:15:13
provided immediately prior the tool call where it read the um contents of this
1:15:21
file right does it know that that path means a transcript well it called the
1:15:27
files read function oh um it called the files read function let
1:15:34
me just dump what this file says yeah and then that way we will know for sure
1:15:41
CU this is one of the things that I had to um I guess hack is that
1:15:52
um I shortcut how some of the things
1:15:57
work um for reading so that it goes straight into the uh straight into the
1:16:05
thread without without going through the artifact uh actions it it doesn't
1:16:11
actually reply as an action it just stuffs it straight in okay and uh well
1:16:17
the probably um it's looking at it and saying um that's a path thank you for that path uh can you give me the
1:16:23
transcript this was the transcript here yeah and we've H God we've run out of
1:16:31
buffer so that's sort of annoying [Music]
1:16:37
um and then oh then I read the whole this was the thread it read the whole
1:16:43
thread to so the messages um analyze blah blah
1:16:49
blah that was the prompt then the assistant said YouTube Fetch and then
1:16:55
there's also this I just want to point out this new parameter that's coming from open AI called refusal that
1:17:02
sometimes the bot will stop and it will refuse to do what you asked and that's the flag there is yeah I've seen that um
1:17:09
I usually just say go on and'll continue um okay so it called the tool
1:17:16
it ran the tool the tool returned and then it said um assistant
1:17:23
tool call read so it tried to read the transcript the transcript paths match
1:17:31
exactly so it did a good job there it's got the um and then the
1:17:36
content came back and it was like details title but then
1:17:45
Subs is a key so it needs to maybe know that within that Json file it's got
1:17:55
[Music] um Subs is the transcription Subs is the
1:18:01
transcription I think is bit say okay right so St it um you recognize the
1:18:06
transcript by the key Subs okay Christ am
1:18:13
in so a bot that helped with this would be able to point out what you're doing
1:18:19
right it's like right you know like exactly exactly it's like uh it's exactly what you're saying but I'm
1:18:26
saying is dipping it wrong it's like uh you haven't told it what what transcript is or the fact that Subs is the
1:18:34
transcript CU it's not obvious that transcript equals Subs
1:18:43
no I you know what I can do
1:18:49
better I'll just rename the [ __ ] variable how about that
1:18:55
how about that to how about transcript this is now going to be called
1:19:02
therefore oops uh trans [ __ ]
1:19:09
script here we go all right
1:19:14
okay I have stick that in your button SM a warm feeling about this one but we'll
1:19:20
see I've lost the ability to have warm feeling
1:19:28
I think pretty early on in my coding career I realized that if I had to pray my code
1:19:34
[Laughter]
1:19:39
sucked oh it's still asked for give me the transcript give me the
1:19:46
transcript so I should I should who's asking that at what point why are you
1:19:51
asking that in the process you must call function
1:20:02
to
1:20:11
yeah uh yeah I'm what doing mistyped the first
1:20:17
transcript although it's pretty good at M typing actually yeah it's pretty good
1:20:31
okay how's that okay let's give that one Let's
1:20:39
uh what are you doing oh God bot programming it would be
1:20:46
so much easier if we had a bot to do this oh work on that one I'm really
1:20:51
working on that how three is just like the start just a
1:21:01
start okay you go please give me the transcript right okay so one a second
1:21:08
what was so just above that if you go back just above the please give me the transcript what was so this is obviously
1:21:17
a transcript this is all the J this is the Json object that came back
1:21:22
yeah um gosh you do talk a lot right okay so that was a tool
1:21:32
call and the assistant had asked to read this
1:21:38
file I gave it back this file the content was [Music]
1:21:44
um uh bracket
1:21:50
details bracket descript
1:21:55
close bracket transcrip
1:22:00
the which one this one marks yeah this one uh because the quote marks need to
1:22:06
be escaped because oh all right okay yeah yeah okay f um is it cuz it thinks transcript
1:22:14
isn't the interesting thing is that this is all Tech there's no speaker identification there's no time stamps
1:22:21
it's just one big long thread uh it might be thinking that transcript
1:22:27
that it doesn't make sense to be a transcript um uh why not just dump the entire contents what of it uh and not
1:22:35
call it a transcript oh well transcript is fine right but uh okay so you got two
1:22:42
call that's giving all of all of this text yeah um if you were to like simp copy
1:22:50
and paste that into a dumbo it would work out right it's like
1:22:56
so what you're trying to do is uh strip out the transcript part and leave the details in the title that's right but I
1:23:03
did sort of want that CU it's like this is extra information about the thing
1:23:09
yeah but that's that's fine you think it's confusing it you so I you just want me to return only this
1:23:15
text yeah uh no no uh I um return um
1:23:20
give it the entire contents what under content just give it give it all of it that's
1:23:27
what it got this this content went back into the bot from from this point on everything
1:23:35
got that's now context straight back into the Bots thread okay but the prompt
1:23:40
is saying um get the transcript yeah uh from that um where it's uh get
1:23:49
the um the contents of the file uh I'm I'm not withth you sorry I'm
1:23:56
sorry um if you go back to the uh The Prompt where uh it's like in the me bot
1:24:03
okay so I see this access the transcript you must oh look look at that look at that example transcript
1:24:10
format Ah that's my old format which just does not apply and
1:24:18
then it's like well you didn't give me a transcript so right right oh good spot
1:24:24
good spot okay well a bot would have got that right a bot would have got that EAS easy one is to cuz being giving an
1:24:31
example is a nice thing but it's not necessary so strip it out run it see
1:24:37
Happ strip this whole thing yep EXC me mate your cough sounds like
1:24:44
mine oh I've been a bit ill heav you yeah just a
1:24:51
virus don't [ __ ] die that a l will kill me one the two are we don't really
1:24:58
care other people
1:25:03
do some IR
1:25:09
here man this is painful and fun still didn't
1:25:16
work where did it fa
1:25:24
did you uh strip strip out all the example from the
1:25:30
meetings so I've got the
1:25:37
um please give me the transcri please give me the transcript this one it's
1:25:43
it's got a definition in its head so what's happening here is it thinks it knows what transcript is more writing
1:25:50
and saying that's not a transcript you asked me for a transcript please give me the trans script so there's something
1:25:57
around the definitions now examples are like proxy definitions is that I'm not
1:26:02
going to Define it uh however here's an example and work it out so um if there's
1:26:08
anything still meeting part that's an example that might be throwing off um
1:26:15
the flip side of it is we could give it an example
1:26:20
um and say you know here's what you're looking for this is what we mean by transcript but the um this is a
1:26:26
definitions problem which is why i' be banging on about uh definitions uh example interactions no
1:26:34
that's fine that's not talking about transcripts answer Y is there anything further
1:26:41
down fine oh that look at
1:26:46
that there is there is ah ah God
1:26:55
oh God okay trying poor bot there poor trying to do it he's just trying to do
1:27:01
it it's so good right like it's just it's just it never ever does things that
1:27:07
are unreasonable yeah like even when my buddy got called
1:27:13
a [ __ ] he uses the word [ __ ] a lot and he's also very sarcastic so what he must
1:27:19
have done is said I love being called a [ __ ] and then it got stored in memory and then the pot came back and was like
1:27:26
enjoy your cocktail [ __ ] and they're saying don't C up Mor
1:27:32
and then it goes back into dog right it was I'm so sorry I'm so sorry okay there you go buddy here it is
1:27:43
right so we've yeah we passed the test there you
1:27:49
go the assistant mention developing a comprehensive blah blah blah okay
1:27:56
so what was the output here the output uh I'll just grab all that and
1:28:04
put it into something nice and easy on the
1:28:17
eye okay
1:28:35
that is exactly why our testing first thing is important right and testing
1:28:42
with variations as well on my ADD yeah yeah because
1:28:47
um that would have been well it was what half an hour of trying to figure out the fact that
1:28:54
we' actually told it to something that we didn't want to tell it yeah that's my bad cuz I just lazily copied and pasted
1:29:00
all your stuff no but people are going to do that I know right it's a
1:29:05
reasonable thing they want to do I just like I just want to get going like a can I use that but over here the video title
1:29:18
outline there you go that seems uh pretty reasonable and uh
1:29:25
in the in the running thread can you ask it questions or uh no because it just ran the test all
1:29:35
right okay fair enough fair enough but that seems a reasonable first
1:29:43
chance so um in a single shot meeting B what then um D is asking questions like
1:29:50
uh was there anything discussed that wasn't answered um was there any you know
1:29:55
fallacies uh any ambiguities were we using the right the um definitions uh in
1:30:02
the right way um so you can get quite a lot of nuance uh once you've got the um
1:30:09
uh transcript you can interrogate that transcript like um a live meeting right
1:30:16
uh so what you're asking for there is um the ability to run a
1:30:21
test go through all the different variations that happen and then jump into to a
1:30:27
thread and Carry On Right talking right see even even in
1:30:33
this setup with the uh the test you've got I mean I don't know how how quick you could do this but if you can run if
1:30:39
you can add another test in the very next thing saying uh well let's go with that um was there anything discussed uh
1:30:47
or um asked that wasn't fully answered let's see because it's script
1:30:54
and it's uh is giving you here's the main point but then it's like let's drill down so what do you want to do
1:31:01
buddy tell me uh so uh having brought in that uh transcript yeah um and uh it's
1:31:09
produced the uh initial summary which we just looked at yeah the next thing would be to give it a prompt uh that would be
1:31:17
um yeah uh give me um a list of uh all
1:31:23
the questions that weren't fully answered any ambiguities and any definitions which
1:31:31
appear to talk about the same thing but used
1:31:37
different words to describe them let see I forgot the rest sorry uh give me a
1:31:45
list of any questions that were asked but not answered any ambiguities any logical fallacies
1:31:57
and any time where a similar topic was talked about but which
1:32:05
a different definition appeared to be used so basically where did we get
1:32:11
wrong you know there's all sorts of ways into yeah yeah okay so uh I don't have
1:32:19
the testing framework in place to actually do the continuation of the next
1:32:24
test case yet cuz I've only been running a single test case in these scenarios so that's why I have to pack it into the um
1:32:32
original prompt as one one prompt here so that's that's the reason for the
1:32:38
shortcoming uh I fix it soon but this is pretty cool right like I mean it's really [ __ ] cool it's
1:32:45
like testing cuz uh uh when I find um when I going into meeting B I use it a
1:32:51
lot right I'm asking the same questions right and so what I the point of this was that if I can get this test
1:32:58
going oh what the fluff
1:33:04
what what you seeing um
1:33:14
error T testd it's not changed
1:33:25
it called the function
1:33:33
wrong I don't know probably called the function right but for some reason it didn't work sorry it called the
1:33:39
functions different hey um
1:33:45
TMA you're calling
1:34:02
H where did the air come
1:34:08
from test path must end with get TPS and the test case
1:34:13
Runner test case Runner
1:34:25
so I'll just add an extra error in
1:34:32
here it seems to be doing the right thing but
1:34:43
uh that could be something I haven't seen before but I've been
1:34:50
dreading is that the B
1:34:57
um with a slight change to a prompt it starts calling the functions
1:35:04
differently with different parameters uh um need to lock that down
1:35:11
why is it doing that I shouldn't um so it's either I've coded
1:35:16
something wrong but I didn't do I didn't change anything from the last successful run I just added to the prompt yeah well
1:35:24
that's that's B free um because it do so it tried to
1:35:30
call to
1:35:37
call it tried to call the meetings agent not the meetings test
1:35:47
file so that's the issue there okay and
1:35:57
so that I'll take you to the prompt that's doing that this is um we're into pistol
1:36:03
whipping torturing you yeah having said be nice to your Bots you got to
1:36:17
Pistol this is this is this is extremely helpful for me by the way because it um
1:36:23
was quite fun well uh I could do this all you can see where I struggle and you
1:36:28
see what the process is yeah so I need to go into fixtures and I think I need
1:36:34
to wipe this out uh test fire Runner test no no
1:36:41
no okay no ignore that so this is the this
1:36:48
is the agent that's running okay yep
1:36:54
and it is looking for test. MD and it needs to it got told what to
1:37:02
run because uh let me show you what it got told to [Music]
1:37:16
do okay so this file that I just showed you got told called with
1:37:24
this single argument this this is the text that went into it all right and
1:37:30
wrong with there it's been prompted to you will be given a file name read
1:37:37
this and then run the test within it but it read it read something completely
1:37:44
different like it read so there there's two possible paths here uh well there's probably more but um uh so
1:37:54
inside of meetings test. MD yeah have you told um the previous bot what a test
1:38:01
is here's an example of what the test format is yes example absolutely okay so
1:38:07
it knows what a test format is and when you say read this test and I read the
1:38:12
file it's like that's a test happy okay and it got this it got this
1:38:19
bit correct yeah agent
1:38:25
okay path uh and [Music]
1:38:31
then add case it got that correct
1:38:36
too and
1:38:42
then um and
1:38:48
then it said this place was where it made a
1:38:54
mistake test case [Music] Runner
1:39:00
test so and it called path with the
1:39:05
agent not the test file so let me go and check my definition in the function yeah
1:39:11
um who called that test file Runner right test case
1:39:17
[Music] Runner [ __ ] [ __ ] that oh man I
1:39:24
love this [ __ ] I really don't do love this [ __ ] path the path to the test file
1:39:32
being
1:39:42
run why are you constraining the uh the naming of the file why not just
1:39:49
say uh use a test file and then it knows you could call
1:39:55
it text yeah um read it it's a good idea to well for example if I didn't do that
1:40:02
then this error wouldn't have occurred this this is actually wrong like it it
1:40:09
tried to call the test Runner with the path to the agent file instead of the path to the test file well no the um
1:40:18
that would still be an error but you're constraining it to um the file name yeah
1:40:24
whereas it's uh you can call it you know j. text so long as it's actually a
1:40:31
text sorry uh actually um a test what does it care you call it anything you
1:40:37
want test. MD is uh something you know you just create it doesn't actually add
1:40:43
anything semantically syntactically sure it's easier for us but why constrain it to that pattern
1:40:53
why not um point it to an email that includes a
1:41:00
test [Music] um you see what I'm saying um I'm
1:41:07
probably not explaining it right but the more constraints that are unnecessary for the
1:41:13
bot the more it's going to get weird um so what it's looking for is a
1:41:19
test file now you've told it the format of a test file you can recognize a test F because of this
1:41:25
format if I were to uh take a a written
1:41:31
um piece of paper that was properly formatted as a test sent it yeah uh an
1:41:36
image you should still run that test doesn't really care what T
1:41:45
um yeah but my angle for doing that was that I
1:41:51
want to be able to have multiple test files all across the file system and be
1:41:57
able to identify them very rapidly without anything sophisticated so you know like if I'm
1:42:03
not going to read every single file in the file system because that's too big but if I introduce a convention that
1:42:10
it's just everything ining in. test. MD then I can do a very quick sweep and then fire them all up that was why
1:42:17
that's why I was doing that enough uh but that's a kind of indexing uh so
1:42:24
piece um which maybe you want to read every file maybe you just want to read the file names and so on but when you
1:42:29
feed it in all it needs to know is uh what's the format of the is this a
1:42:35
test it doesn't need to know that you've named it right so um the um yeah but the
1:42:43
the agent that error of saying that the file name was incorrect that was on
1:42:48
artifact side that was not on um bot side oh see I see yeah yeah
1:42:55
okay um okay here we go here's our next thing
1:43:01
so that prompt ran the way I fixed that was I modified the function definition of what path was
1:43:09
to be very explicit that it was the test file I I can understand how the bot got
1:43:15
a little confused there it was not clear um I like to imagine that a bot you will
1:43:22
make us in the future sure we'll cover that yeah but so all I did was I I said
1:43:28
I changed this to be run yes and I I I gave it a
1:43:35
rigix as well and said the function parameters must end in. test. MD and so
1:43:41
that gave it some extra impetus yeah so artifact knows uh as you're saying on
1:43:46
the search it's not test. MD it's not test uh you give it over through the bot
1:43:52
the bot doesn't care what it's called but what does care about the format is this actually a test yes yeah
1:44:19
okay here we go here is the output
1:44:25
right yeah I don't know what happened there good I don't know what
1:44:32
happened what did happen there uh that not something to it passed
1:44:38
the test right um okay so it's added a fourth one which probably a whole bunch of ums and
1:44:44
ass oh no it was fine that was an error in um that was an error in my bot the the
1:44:53
GitHub co-pilot that didn't do what I asked wow um so you've got uh an input
1:45:03
oh no look it just there I see what it's done okay put in a little bit of
1:45:11
a oh there's four yeah okay right it added in some white space there you go
1:45:18
yeah okay we all cool we all cool
1:45:27
I'm so looking forward to when we're actually just talking about because it just comes down to how sharp
1:45:33
your mind is and nothing else it's beautiful it's a beautiful
1:45:40
world to inhab it's coming buddy it's
1:45:50
coming okay is this the new um or the previous this is the new one okay so
1:45:56
it's missed the it's not done the um next steps oh God you're right it
1:46:01
isn't yeah what the
1:46:16
fu next steps unanswered questions ambiguities logical fallacies and discrepancies and definitions
1:46:24
did I not copy that
1:46:31
right I'll I'll grab I'll take that whole text over for you and then you can have it in a something a little more easier to
1:46:42
digest there you go we we asking to best dig
1:46:54
steps unanswered questions oh so this is actually not oh I'm sorry
1:47:01
I appear to have really [ __ ] up yeah you're you're getting prompton
1:47:09
out poop mashed I copied the wrong thing that's what I
1:47:16
did sorry my bad there you go there you go good part good part
1:47:23
good bot good bot biscuit yall need a big ass
1:47:30
biscuit there we go
1:47:36
hey oh right we users most desire in the state
1:47:42
board so someone asked that and then someone didn't wasn't answered uh this is the thing um uh I
1:47:52
think uh uh well let's let's keep going with this cuz this is awesome but um having delineated uh who
1:48:01
the uh two speakers are or the multiple speakers are yeah can be really useful
1:48:06
but the other really useful thing is to put a time stamp in because if you go back I get I I I I can get time stamps
1:48:15
out you can oh that's really great because thing I I would ask is uh um
1:48:22
right um where was that thing you just highlighted that's not what you're is it no no um in the output it was uh an
1:48:31
unanswered question what specific features or functions right okay so the next thing
1:48:39
typically what I would do is um take me to the point in the transcript where
1:48:44
that question was asked consider only that topic and uh give me a summary of what I
1:48:52
said so there's a couple things it needs um it needs to know who I am um and need
1:48:57
know the timing and what that does uh yep I got you buddy I can do that for
1:49:03
you but you're going to need to help me with some Bing uh the reason I was doing all this is because I was going to get
1:49:09
this test passing just enough to know that it sort of worked sometimes and
1:49:15
then I was going to publish it so that you can have it in Long threat and you could then oh man that' be awesome
1:49:22
that's what I was trying not going through it but yeah yeah I've got I pulled
1:49:28
out uh complete list I had to do it manually but it only took half an hour
1:49:33
um of uh the uh URLs for all videos of the last 6
1:49:41
months right so that's what I was leading up to I was like well we can get these Bots going to just haul that stuff
1:49:48
in and then you can sit there asking top level questions like okay go through every video and find every unanswered
1:49:54
question list it in chronological audio audio duplicate it between all the
1:50:00
videos give me the links to all of the most important ones that's right that's
1:50:05
what you want that's what you want buch a whole bunch of really rich stuff I'm really Keen to do things like um uh if
1:50:12
we're talking about something similar and we've changed the definition Give me a summary of the reasoning why we did we
1:50:18
made that decision right okay some really rich stuff there all right so just um give me
1:50:25
just half a second and I'll figure something out
1:50:31
yeah oh uh it's really odd to listen to your own voice uh I'll ping this
1:50:41
over well this is like what are you sending me what are
1:50:47
you doing um no this is just uh I can do
1:50:53
it afterwards what it is is uh I was saying over the last 6 months what are all the
1:50:59
um uh the um URLs to all conversations
1:51:04
um in chronological order with time stamps uh yeah I um I can I can deal
1:51:11
with it on this side deal on that side that's an easy thing because it's
1:51:16
formatted it's well well it's roughly well formatted
1:51:32
interesting thing would be the list of tests for each of our
1:51:39
conversations would be what what would be a fail on one of
1:51:44
our conversations if we never came to a conclusion if there are too many
1:51:50
unanswered questions if we are just talking fock need some kind of field parameters
1:51:57
there which should be interesting unit testing uh meeting or
1:52:05
recording huh oh I'll help
1:52:20
you okay I've got I've got an idea write that down my
1:52:28
P oh that would be
1:52:35
awesome oh that would be good I've got the next version of Mee
1:52:41
and Bot coming oh yeah yeah yeah okay yeah yeah
1:52:49
I got it got it for
1:53:43
what's this like a magic number what's what's that
1:53:57
usually hours minutes seconds uh I found if you put HH
1:54:02
mm it works okay
1:54:15
cool um you probably want to see uh we'll generate the link uh with time in hours minutes and seconds to in minutes
1:54:23
and seconds because that's ambiguous like what I do with minutes and seconds
1:54:58
sorry buddy I'll get there I'm just uh no no change or whatever why not make
1:55:04
the top shut up I'm trying not to back seat D It's hard hard to watch is
1:55:13
it I'll let you finish your thought and then I'll suggest a couple
1:55:21
things okay right hold on no wait wait My Clipboard is full My Clipboard is loaded okay just
1:55:29
let me let me just
1:55:55
okay and now what do I do uh right um do you have an sample of
1:56:00
the time stamp yeah inad of saying 933 um put
1:56:08
in uh like from a real thing yeah just a random time from YouTube okay uh let me
1:56:17
let me then let me run this while I go figure out the rest of that thing yeah
1:56:22
uh well okay here it is here it is here this is this is the format here uh start
1:56:30
duration seconds yeah duration in seconds and then the text all right okay so uh we
1:56:39
you say that uh start is there may be several relevant sponses
1:56:44
for example for response give if possible you uh remove it if possible
1:56:51
just how it to to um generate a YouTube link uh to the
1:56:59
time that's most relevant for that response um there may be several
1:57:04
responses um an example uh so where you got four example
1:57:12
example of a relevant timestamp
1:57:20
is is um yeah so active versus passive voice right exactly y um you go down I
1:57:29
get rid of the started uh or um uh which
1:57:36
uh yeah yeah yeah yeah yeah good good yeah um it's like uh this
1:57:44
means uh it was 950 seconds from the
1:57:50
start and the uh duration of that utterance
1:57:59
utter yep UT that section utterance was
1:58:06
5959 you are to translate that
1:58:11
into HH mmss where the start is
1:58:18
000000 0
1:58:33
uh can you sorry uh yeah do that b uh change this means um in this to in this
1:58:46
example uh uh it was yep um
1:58:54
X
1:59:00
was the start and the Jan speech
1:59:05
was yes okay you are to translate that
1:59:11
into hhmmss where the start is 0
1:59:26
oh that's a good one that sounds like you learned that the hard way oh
1:59:31
God yeah oh yeah oh yeah you've not been
1:59:36
bleeding alone with [Laughter]
1:59:44
mey doie uh why why you giving that um a link at the end cuz this is how to form
1:59:51
the links that give the links to so that you can click on it and then it takes
1:59:57
you to that period in the video okay um yeah but you mean to uh say that that's
2:00:04
what it is um an example in this case would result in a
2:00:12
link such as this
2:00:22
yeah yep and uh you can get rid of the uh the HS
2:00:28
mmss uh yep
2:00:35
and yeah why uh because you've already told it what hm mmss yeah but this is
2:00:42
the format of the link oh I see oh okay all right um yeah so okay yeah yeah that
2:00:49
should work y okay
2:01:04
burn tens burn someone's getting rich someone else
2:01:12
is going to jail what was that song Going To Hear KN someone's going to
2:01:19
chill
2:01:27
s lies drugs and money
2:01:38
um it might be generating a lot of links
2:01:45
um well you can offload that uh because
2:01:50
uh so long as it's well form m in the HS mmss uh then you can do the um Navigator
2:01:58
prompt it saying if I say go to you know uh 10 minutes and 30 seconds
2:02:06
you don't D Link you don't you don't need to click you should be able to just talk to it this has been running for too
2:02:13
long I don't like it yeah stop it yeah it's probably burned a lot of
2:02:19
tokens uh so yeah oh take out the link the link or the whole
2:02:25
thing um no no what we want to do is to get uh the time stamps into um it
2:02:33
understanding can can we just check that
2:02:39
um oh wait I left that in there by mistake my
2:02:45
bad not that that should have made a difference not sure that would have made much difference it would just confused
2:02:50
it can I try cuz this is the first time I've
2:02:55
returned the um I've returned the timestamps so we
2:03:02
don't actually know if it works with the new timestamp return format so can I
2:03:08
just try it without the request for the YouTube link and just make sure it still
2:03:13
works even though the yeah yeah yeah yeah yeah because this is this is actually easy this is like post
2:03:19
formatting uh because if we assume that uh YouTube format is consistent we can
2:03:25
transform it to whatever we want yeah so it also dawned on me too that what we want is to do a presentation
2:03:33
pass and I hav't spoken to about this before but we should get the agents to
2:03:39
be correct and then display the correct result to the user while at the same
2:03:46
time tripping off a presentation layer or transform that transforms it into
2:03:51
something based on the users's preference or the company's preferences or something like that so
2:03:59
that you know but and then when it comes in it just replaces what was on the screen so it it doesn't feel like it's
2:04:07
taking too long that'd be nice I mean that's that's not core but also uh well you know the Yanks um always get their
2:04:14
uh date time stamps wrong uh uh mix up uh these and uh months for
2:04:23
some reason oh what what what this model's context length is 128,000 tokens
2:04:31
however your messages resulted [Music]
2:04:36
in what no I use too many
2:04:41
tokens what's your what Your maxed out of tokens at also that doesn't make sense it's
2:04:48
like I thought this is 4 mini oh uh scroll to the right resulted in two it
2:04:55
wraps around to there 267 629 tokens oh I see all
2:05:01
right uh really
2:05:08
how how why so many the input um what's the
2:05:16
um you look at the the rod dump from the
2:05:23
transcript uh it was big I can dump that to this I can put that out in the log
2:05:30
okay well we assuming it's like big that's fine um so
2:05:37
128 is quite a small number of tokens in the grand scheme of
2:05:44
things 128k I thought the window size no that is the context window size isn't
2:05:50
it let me double
2:05:55
check to be honest I always just like put it up to
2:06:09
Max yeah okay a mini um for mini yeah what's
2:06:17
what's the Restriction well I'm getting I'm just on platform yeah I'm getting a lot less
2:06:23
than uh what what is the number give me a sec it is uh 16383 Max talks no that's
2:06:31
not that's not the answer yeah yeah that's a limitation of the web
2:06:37
UI uh let me look this up in the docs for the models um well if I to switch that to
2:06:46
models 40 mini context window 128k okay so we busted through that
2:06:53
uh they're all 128k I don't know why I thought they were bigger
2:07:00
um um I've tokens problem in ages or weeks well I'll dump the I'll
2:07:09
dump the file of the disc uh the file size for
2:07:14
you yeah
2:07:24
they changed that no I I thought it was bigger but maybe I'm
2:07:29
wrong I thought it was bigger as wrong so would both wrong or have changed
2:07:43
it okay here we go whoa whoa whoa whoa slow down buddy slow
2:07:49
down um ah well I ran out of my buffer now so we could uh strip out
2:07:59
duration anything you want to strip duration yeah
2:08:07
I can do that it by
2:08:17
roughly so we had start
2:08:28
um oh we talked about duration du so I keep start and D
2:08:38
are and text yeah
2:08:44
it's it's not going to say much no it's not um
2:08:53
we try anyway see but uh that's a hard limit which is uh because sometimes we
2:09:00
do bang on for many hours um okay I'm going
2:09:07
[Music] to how would
2:09:12
we we would need to chunk it in this case right yeah but
2:09:22
who wants to chunk who wants to chunk indeed buddy yeah cuz we could chunk it and then next week they go oh it's a
2:09:29
million tokens I could just SW it was more anyway
2:09:38
um well for this example probably just choose a shorter
2:09:44
video doesn't matter who the video is just choose one random like 10 minute video as a URL
2:10:03
it does seem like it's eating too much though
2:10:14
yeah it's good for you to see the pain I have to go through like it's real fiddly
2:10:20
to make this whole thing work together is good for me to actually feel your pain like is Lally more pain than my
2:10:28
side like thanks for that man uh i' much rather think that you
2:10:34
know you have no pain and therefore I feel good about myself oh and you now you're like
2:10:40
actually yeah that whole empathy thing that that generates a lot of
2:10:46
tokens so the size in bites was 178 ,000
2:10:53
bytes which means that it should not have busted the tokens like it was not
2:10:58
even close no um is this run still busting the
2:11:04
Tok this run hasn't made it there yet there might be some errors in the
2:11:12
API oh yeah yeah the API is uh well not completely to be trusted um
2:11:20
it's FL as hell man yeah but you know Innovation all that kind of thing yeah
2:11:27
yeah major outage 35 minutes oh dear impacting
2:11:34
Lin for5 minutes it's nice to know that the chat
2:11:40
gbt and the API seem to be like it sounds like chat GPT is using the API
2:11:48
yeah you know so there's some extra stuff
2:11:54
but more or less they're the same you know you got to uh take a hat
2:12:00
off to you know any company that puts up their outages in a bar chart like that
2:12:06
oh everyone does these days like we're going to do that oh yeah yeah but uh
2:12:12
does everyone do that now I didn't do that well no one did back in the
2:12:18
day instant report
2:12:23
okay so it worked it worked
2:12:30
but I think something else was going on like I do believe that that was a um API
2:12:37
eror because the size of the file you know just isn't
2:12:43
enough um and then what were we going to do meetings
2:12:51
we don't have duration
2:13:01
anymore yeah that that
2:13:08
is that's data that we can actually infer between time stamps I'm not sure why they put in duration strange that
2:13:15
they choose to put that in uh because the next time stamp start may be sign
2:13:21
significantly later than the [Music]
2:13:26
end of the previous time St plus duration cuz if you say something and then go quiet for 2 minutes without
2:13:34
duration you don't know that that was 5 minutes of text you don't know where to clip your video if you want to snip the
2:13:40
end I suppose I suppose um I choose a different way of doing
2:13:46
that but yeah yeah yeah I
2:14:04
suppose okay here we go it's going to work this
2:14:11
time it's going to work it's going to work is it quick go go and sacrifice
2:14:18
it I got a mouse
2:14:25
well I've got a printer to sacrifice later on today which I'm going to
2:14:31
enjoy a you know what you know what I think it's [Music]
2:14:36
um I know what that I know why the tokens were big because I didn't Minify the
2:14:45
Json I I was pretty printing it with like a new line and a tab and all that
2:14:52
you know it wasn't just that's going to be that's going to double the size well actually slightly
2:15:00
more yeah why is this taking so
2:15:08
long it shouldn't be so
2:15:15
slow it's generating a lot of stuff it could be that uh it's just
2:15:21
a bit [ __ ] right now it could be that we're an infinite Loop and you're about to be charge
2:15:31
$127 I was so glad when that was your pro your your mistake not mine CU I was going [ __ ] what I
2:15:43
done I was I was convinced it was it was me cuz I was kicking off Unk know
2:15:49
perimeter parallel toal that's an error on their side man all right okay that's
2:15:55
absolutely a legit parameter that we have been calling for the past [ __ ]
2:16:02
all these tests that you saw around here that's their problem time is uh where's
2:16:07
there um where are we calling for this uh instantiation uh of the API are we co
2:16:14
West Coast I don't know it's calling the one that is closest to me in New Zealand
2:16:21
uh but West CO yeah I don't know but but normally we would hit
2:16:27
um uh Us East when it runs on the deploy platform because we are collocated with
2:16:35
open AI pretty much so that's why it all goes Super Quick all right so you're
2:16:42
saying that uh well number one okay this is uh oh I
2:16:51
have no evidence for but um suspicious that it's uh Saturday and it's early
2:16:57
morning uh on East Coast right now sounds like we're pushing something yeah
2:17:04
and just keep it running while they're pushing which is Bal might be something to do with that
2:17:12
um it's not generating the links buddy oh no it's not not is it
2:17:19
why did you expressly say yeah go back to
2:17:26
their after each response War
2:17:31
okay okay it feels like this is the wrong place to put
2:17:37
it cuz this is like how it's expecting to be used but we've tried to tell
2:17:43
it you know and none of our examples include these um YouTube links I think I
2:17:49
think we we probably like B this one out what would be great is
2:17:54
uh um I think I need to put a link example in the
2:18:03
response right um uh
2:18:09
um right yes possibly uh go example
2:18:14
interactions uh do you have um I think meeting bot's got an example output is
2:18:19
it maybe it doesn't no it doesn't uh summary so action items
2:18:28
the following items in the yeah um we identified and I will say
2:18:35
ah we've not told it the format to Output in so if you go right down to the bottom um you do something like
2:18:44
um uh hash output you are to um output in the the following format
2:18:52
and then what are these three lines for can I kill these um yeah they're probably residual
2:18:58
unless no no no the three lines are just say that's not part of the PR but consider
2:19:04
examples uh no um no examples um
2:19:10
output uh so uh you are to Output in the following
2:19:18
format ah cool on okay so uh HH
2:19:24
mmss no no no can't no why don't I why don't I just why don't I just um cuz not
2:19:31
all of these things can have um these links right right because what we're
2:19:37
asking it for is a summary and there uh the summary by definition involves the
2:19:43
entire transcript so there's no time stamp for that okay so logical fallacies
2:19:49
we can definitely give
2:19:56
one with the um [Music]
2:20:03
uh how do you see that um with the uh
2:20:09
start of where this was first
2:20:19
discussed this was first discuss let's see let's see this yeah yeah we're we're being B at the bot game cuz we're saying
2:20:27
give us a summary and then we're saying give us time stamps is not something you can have a
2:20:32
time stamp with yeah but if you had give it uh where it's got to do the first
2:20:38
time maybe it can get his head run that
2:20:57
it's about 11 p.m. your time what's [ __ ] oh man yeah I'm I'm good but man the
2:21:03
time does the time does roll on this is this is good stuff though
2:21:11
this is where was there anything else I wanted to cover here yeah that's right let me
2:21:16
just uh if we just park this for now um
2:21:22
the the reason why this became a problem is
2:21:31
because what's happening
2:21:36
here yeah yep there's some time stamps time stamps yep okay
2:21:44
okay all right so is trival then to mess around with the
2:21:49
format with it's a link or just seconds or it's not picked up HS mm SS fine we
2:21:57
can that's that's that's true that's fine that's fine I don't I don't mind
2:22:02
that this poor poor
2:22:08
thing I dearly just want to see this so
2:22:19
bad ah yeah well that's good though it's uh
2:22:27
yeah but no no no that's not good because it's got two different formats of time stamp there it shows up as the
2:22:34
selection here because I want to talk let's see if it's right so and if
2:22:41
the okay let me let me just figure out what was the thing that was talking about an appeal to Authority was present
2:22:47
when discussing whether the designed decisions should follow the opinions of established experts without Critical
2:22:53
examination of those opinions what oh and there's a
2:23:00
Fed L there is a potential Hasty generalization when asserting that
2:23:06
because some designs worked well in general they must work well in every situation discuss a hasty
2:23:15
generalization that's a logical fallacy right up there part of the
2:23:22
loes is the ability to select within the thread so like I should be able to
2:23:27
select that message and it shows up as the selection here because I want to
2:23:32
talk about that message right so and if the changing of the stateboard appears
2:23:39
as another tool call can and be like this um it's picked up that logical
2:23:47
fallacy because you said I should be able to as which is aaly but it was an
2:23:55
example I can I can deal with these nuances that's that's over the screen and show however pick up the right
2:24:04
time yeah because that's rollack as well right that's roll back and toggle in one
2:24:10
in one device one mechanism that's cool right okay and then so when the bot says
2:24:17
I am now changing the State Board I will AO I'm not sure it's
2:24:23
wrong you think um I think it picked up you said I should be able to no it
2:24:29
picked up the Hasty generalization because I I Oh I thought that was a
2:24:34
Authority no no I can watch the appeal to Authority one I think I got that right because it was saying that I just
2:24:42
tried to collapse a bunch of solutions to be the same
2:24:48
solution and it called me out for saying it was a hasty generalization because that's what I was trying to do was
2:24:54
generalize it down I had less work that's a valid call out that's nice
2:25:02
okay so the next one the appeal to Authority yeah let's go for that one appeal Authority was present when
2:25:08
discussing established experts without Critical examination of those opinions
2:25:16
okay yeah because that's roback as well and toggle in one in one device one
2:25:24
mechanism that's cool right okay and then so when the box says I am now
2:25:30
changing the state board it hasn't put the time in
2:25:35
there doesn't it uh 8543 what's the next
2:25:44
one um seems to the state board and give
2:25:50
that would um solve your roll back thing so that's that one solve you that would solve your roll back
2:25:59
thing state bo and
2:26:05
give the time stamp's not working what have I done wrong I think I might have
2:26:10
given it the wrong um format yeah
2:26:17
yeah see
2:26:22
uh it looks like the right format you like paste it maybe yeah I know
2:26:34
um so that 542 s a i know it didn't like the it didn't
2:26:42
like the milliseconds ah we didn't tell about
2:26:48
milliseconds I just wonder if if it it's cuz I was like that a point and
2:26:55
I'll bet that that messes up yeah that could be one right that's
2:27:02
what the issue was okay well that's that's interesting well let's um you still want to watch these you
2:27:09
okay for time I'm I'm actually fascinated I've got as much time as you got man you're getting late and I'm getting 8 543 yeah I don't have anything
2:27:17
for a week well okay cool um
2:27:22
8 five 43 we need these nuggets and then I'll
2:27:29
make us a little widget cuz that widget will be I'm making widgets right now anyway
2:27:36
turn to learn about the dream catcher you're actually using it's running dream catcher it is talking to you with GPT 40
2:27:42
possibly mini because if we want to be tight asses and it's like
2:27:48
awesome I know it is epic right and it seems about as smart that's
2:27:55
the weird thing yeah so um and then we yeah that's it so don't worry
2:28:03
about docy Source at all what you need to worry about is the the structure that you want inside the way you just
2:28:09
described and then tell and then I'll you tell me what to make for the the
2:28:14
stateboard widgets I think it's very simple it's just like what we had on the
2:28:20
website sort of and then um I'll put in the button the button bot
2:28:28
and then you can I wonder picking up dogosaurus as an
2:28:35
expert don't worry about yeah it's interesting though isn't it
2:28:42
this is so interesting thank you so 541 this was the other era which
2:28:49
was potentially Hasty
2:28:56
generalization theum right if you attach more than three things what are you doing I guess is the
2:29:04
question so I could make the toggle button
2:29:10
just toggle over toggle over the stack of
2:29:17
things or I could make the stack of things go scrollable or something or I can just not worry about it and um you
2:29:23
know we'll figure out it do hor
2:29:33
scr
2:29:39
okay but the loes are long though like they're probably about that long because they contain things like um file paths
2:29:46
uh
2:29:53
here okay all right so you want it to go yeah okay fine um horizontal it is and then we'll just deal with that um and
2:29:59
the toggle I kind of think of a better way like if you're constrained for space I think it's
2:30:05
right that was a I think it's right between the two of us that was a sketchy time cuz I was
2:30:12
like yeah what you're asking for doesn't fit the UI guidelines but I don't think
2:30:18
it's worthwhile arguing about it so you know I was kind of like whatever and you were like it should be horizontal and
2:30:26
then but neither of us really know exactly and so we just like yeah yeah
2:30:32
yeah okay okay um well look I think that proves some obviously there's some
2:30:37
whipping but yeah can I yeah is there any unanswered questions what would happen uh if B calls I'm just fascinated
2:30:44
I okay time St 852 yeah
2:30:50
that out in terms of forting but to happen if like if the bot calls show
2:30:56
stateboard would you expect that to flick the toggle or would you expect to um simply be told that I can hit the
2:31:03
toggle in I think it's Sim to back chat is it I don't want to have you didn't
2:31:09
answer did you you were just like answer I [ __ ] answer a different question he just went off
2:31:15
and [ __ ] hell that's EMB
2:31:22
so what's your answer to x well given why um oh that is uh pretty damn good for a
2:31:30
zero shot isn't it ambiguities time stamp
2:31:36
378 this is hilarious dude please please not me not me again not me again come on
2:31:42
we should score these
2:31:47
yeah a laptop and a phone yeah that's what I'm talking about yeah reasonable for that um only problem with switching
2:31:54
or you remove the so the issue there was ambiguity the discussion of what
2:31:59
constitutes a big computer versus a small device is unclear oh cuz you asked like what's the
2:32:06
difference between big and small and I was like laptop versus a phone but I suppose that there's some
2:32:12
phones that are massive and some laptops that are tiny well the the thing is um and none of these are um test fils right
2:32:21
um and it's like it's almost it's almost like after a meeting we should have like
2:32:26
the followup where we go through with the bot yeah but it yeah right but it
2:32:32
would be bit that's fine ignore that but something that's a little bit uh passive
2:32:38
aggressive that I would look forwards to doing is um tweaking the bot with my own
2:32:43
personal pet peeves that occur in a meeting and so it would like generate
2:32:49
you know like and if if I could like get the like not answering a question that I
2:32:55
asked I find that incredibly annoying I never noticed you doing that so that's interesting that the bot caught you
2:33:01
there oh yeah no I'm I'm I'm queued into that because sometimes I E no no no
2:33:06
right okay basically uh Park that whatever yeah that's what I asked yeah
2:33:13
um which is really this is so much just interesting
2:33:20
isn't it like if you if you had that system running I would imagine you would make a bot that was like the regist of
2:33:26
the judges that was orchestrated the judges and so that system the thing I've
2:33:32
been toying with is that these widgets can be nested and so you would make a widget that was the um the orchestrator
2:33:40
widget that could be assembled with three different judges that were split
2:33:45
by tabs for example and so you could you could get the three judges to Output their results and then you could see
2:33:51
them all just by Hing on the tab in the widget now you could read the data raw
2:33:57
because the data is all in files but the thing that widget lets you do is sort of slurp that seemed clear to me I think it
2:34:04
might have I think cuz we covered several
2:34:09
different ways to represent the judge's opinions and it's like well which one is
2:34:14
it yes yeah um which is fine because uh the way looking at these things and the
2:34:20
way have been using them as advisories CU you can scan down yeah
2:34:26
yeah yeah yeah they're not all really useful it's really useful dropping into the video I know right really useful
2:34:33
back thing yeah cuz that's roll back as well right that's roll back and toggle in one in one device one mechanism oh no
2:34:39
we covered that one sorry we covered that one yeah yeah but um damn this could be really painfully
2:34:47
useful feedback and instruction ctions unclear boundaries on how user
2:34:55
input would be directly impact the UI adjustment okay all right let's a
2:35:08
look because um IDE remember the idea is your phone uh with the stateboard up all
2:35:13
the time and all you're doing is talking it you don't actually take right so this is how it would look on a mobile
2:35:19
you know and so you sort of want to your stack of loes for interactions would be rising up here but then you'd always
2:35:25
have this toggle button over here that could flick out this area for the stateboard view and back
2:35:31
again so youing right or something that state or the to well I tried to make all the
2:35:38
interactivity of the system is this little area that's where everything happens putting
2:35:45
something in no
2:35:50
more um true are not
2:35:56
matter to me was always in the top right I could always get to know about it right but then we blocked whatever was
2:36:02
up in the top right which is unknown was here you haven't really blocked anything
2:36:07
you can always assure that there's clear space there what was the comment
2:36:13
that discussing that seem different with uncleared boundaries
2:36:20
y so just move no it's more about the fact that we
2:36:27
have dreamed about the state board and mentioned it many times but when it comes to the actual utility of it it can sort of hit a bit of a a lump so anyway
2:36:36
um we're just skirting over that we're skirting over it it's like we can't figure it out yeah that was a it was a
2:36:42
very vague thing okay well that is fascinating and for a first pass that we haggled together and
2:36:48
likey is without a bot that could have saved us much of that round and round
2:36:55
like you know detecting conflicting instructions in a pot um you know that
2:37:01
that should have been a tool that helped us for it okay so you cool if I move on
2:37:07
to my problem um I just like to bask in the uh beauty of BS the warm think about
2:37:14
how how would you do that uh in terms of hiring someone sit down and do
2:37:25
what complete transcript and then figure out all the ambiguities and then hand it over to you and then and make some
2:37:32
links yeah yeah but that was pretty good so so I mean like that those links I
2:37:37
mean they're clickable and they'll be clickable in the um in the message list but
2:37:45
ideally uh I'd also be able to show them in the board so you'd have them all sort
2:37:51
of you know just stacked up with all the videos and then you just I should be
2:37:57
straightforward enough Ian we're not breaking anything that we've been talking about no I think no um and the
2:38:04
uh it's pretty cool on the on the prompting um for example if there is an
2:38:11
un answered question say if we talked about one thing went down a rabbit Hall came back to talk to the same thing what
2:38:17
i' want to know was multiple areas but we've just said the start time yeah but
2:38:23
that's that's that's do that's that's just uh yeah so that's really cool and
2:38:30
so what I think would be fun to make is um taking something
2:38:37
like so Seed Studio here allows you
2:38:43
to purchase basically the hardware components that you need to make some
2:38:49
really cool stuff uh so if I go no more
2:38:54
than that so if I go to um
2:39:05
uh re speaker here we go mhm so you can buy things like this
2:39:14
little case and this is like a um this is is like a six mic
2:39:21
array and it fits in that little little case and and it's got a little raspberry
2:39:27
pie in it and so what we could do is have that sitting there on our desk when
2:39:32
we talk to with people and it do the transcription and feed it into how I was
2:39:38
about just talked about I didn't know about these guys but yeah live doing it live yeah but also it would have so what
2:39:46
this thing can also do is these LEDs it it does what's called um uh speaker
2:39:54
Direction I forget the acronym for it but it does speaker Direction which means that you can know the LEDs light
2:40:03
up based on which direction The Voice is coming from okay and so you can use that
2:40:10
to yeah but you can use that to split the audio streams so that you've got speaker
2:40:16
identification nice and clear um yeah so so basically you and I could
2:40:22
sit in a room we put this disc this device down and then we start chatting it splits our streams off has our
2:40:29
individual hows populated with what we said and then we are now effectively
2:40:34
having a text meeting as far as how is concerned and it's busy running these analyses on the side be wouldn't it be
2:40:41
cool if uh it's running the transcript um you know every X seconds and saying
2:40:47
hey you guys were starting you're getting somewhere and you were talking about this but then you just dropped the subject yeah yeah and in being able to
2:40:54
see these things pop up on the dashboard while we're talking I think would help us to not miss anything cuz you you
2:41:00
don't know what you missed because it's it's dropped out of your memory but if a machine was there being like hey this
2:41:07
thing that thing um so these are pretty fun things
2:41:12
to toy with I don't think that'd be very hard to make and it's really just hooking up a they're just raspberry pies
2:41:18
aren't they yeah just them yeah and then just pipe it up to
2:41:26
H yeah yeah yeah that's sort of where I'd the next time we meet in person we
2:41:31
should have these tools I think it would be so cool we have an alarm going Max you're
2:41:39
talking BS and then like three strikes you're
2:41:44
out like if you talk [ __ ] for more than three fallacies and it's like
2:41:49
meaning is over okay so the the the whole issue
2:41:55
that I was bringing that up for which is still blowing my mind that that all worked and we were able to twiddle that
2:42:03
together so quick and this was the test file for it that was plain text that's
2:42:09
pretty fun the reason I wanted to bring all that up back to
2:42:16
my drawing here is um
2:42:22
that so say I'm in I'm in now this whole thread is going to be
2:42:28
in how okay and I'm going to use the colors to represent which agents got switched out by the switchboard right
2:42:35
okay so this is the model of one laptop the one laptop model uh yeah you're in a specific office and this is how the
2:42:42
agents are being moved in and out of the room for you yeah okay so you're like
2:42:47
chat chat chat and and then in that example you
2:42:56
go I want to analyze this YouTube meeting duh okay so then switchboard
2:43:04
ought to kick in and say oh you want the
2:43:09
meeting bot and then it switches over to meeting
2:43:15
bot meeting bot looks at the request and says hm
2:43:21
that's a YouTube transcript and so different to how I presented it to you
2:43:27
cuz I I forced meeting bot to be an expert in YouTube videos and a lot of
2:43:32
our a lot of our [ __ ] around was trying to get it to pull in YouTube
2:43:37
transcripts be generalized but to expand that further
2:43:42
it might be pulling in from some other source like maybe I'm like I want to upload an audio file okay I want to I
2:43:50
want to you know there's a whole bunch of other things that you might want to do and so to modularize meeting bot it
2:43:58
should know about another agent called YouTube
2:44:04
transcriber yeah and YouTube transcriber so
2:44:10
switchboard toggled over to YouTube bot YouTube bot of its own accord said oh
2:44:18
this is a job for for this is a job for sorry how
2:44:24
switchboard called meeting bot meeting bot said this is a job for YouTube bot mhm and it of its own accord caused
2:44:33
YouTube bot to take its place in the thread and now this is important because
2:44:39
YouTube bot starts YouTube bot goes about it sort of
2:44:45
predetermined drone like activity YouTube bot hits a snag that needs some
2:44:50
input from the human and so what I would imagine happening is that if YouTube bot
2:44:56
was prompted in such a way that it could interact with the human to get specific
2:45:03
details then the human responds YouTube bot does its stuff it
2:45:09
can finally complete its task and then YouTube bot signals
2:45:14
completion which means that the stack gets popped and the result goes back to
2:45:21
meeting bot who can now proceed with further interactions with the human that
2:45:27
seems reasonable because uh basically what you're um ditching is all the two and throwing nonsense trying to figure
2:45:36
out and um the uh the bot itself should be able to give you a good summary of
2:45:41
what decided exactly the same way as meeting B just did right it took whatever it was an hour two hours worth
2:45:47
of transcript and said okay here's thing now um if the
2:45:54
trans if the summary the pop um uh doesn't answer uh Dave's
2:46:03
question I think he should still be able to um interrogate the
2:46:09
full stack so let's say this was meeting B right so um there's like uh meeting
2:46:17
bot blah he's meeting uh orange orange orange orange orange okay so here's a summary right fine we're now back into
2:46:24
talking about logical fallacies that sort of thing and then um saying I
2:46:29
should have said this but it wasn't in summary so it should be able to go back
2:46:36
into into that so by pop we shouldn't be losing data there it should be some way
2:46:41
of pulling back uh the data that wasn't summarized
2:46:49
so the job here was pulling in the Raw YouTube data
2:46:57
and you're saying that you uh the meeting bot should be able to pull see all of the raw data it
2:47:05
should be able to go back to primary source I think I think yeah but this this chat was about generating primary
2:47:12
source so what got generated was primary source um oh okay so slightly but yes
2:47:21
it's a very good point um if you're generating primary source then at the end of that orange um set You' be going
2:47:29
uh yep okay that's good that is now canonical that's the thing that happen
2:47:35
yeah yeah yeah and then you can collapse all that uh you might uh this is pretty
2:47:44
marginal you might want to be able to go back and seeing why did you collapse it like this right but we don't have to
2:47:51
worry about that yet yeah okay all right so I'll add in the functionality that
2:47:57
allows for one agent to invoke
2:48:02
switchboard to force a switch to another agent that they know would do the job
2:48:08
better and then instead of invoking it like a drone which is like how the test
2:48:15
file Runner agent gets called where it does it is not permitted to talk to the
2:48:21
human um simply because that particular task doesn't need a human to talk to it
2:48:29
but uh also it's designed to run in huge parallel numbers and so that would drown
2:48:36
the human but for for other tasks that are non- drone like one agent
2:48:43
[Music] can switch the thread to another agent
2:48:48
and then have it switched back to itself once the task has
2:48:55
completed uh yes now uh not this is not meant to be a
2:49:01
confuser but uh referencing a last conversation um it would be reasonable for you're talking to Orange and uh uh
2:49:11
orange uh kicks off three completely different Bots and different models with the
2:49:17
temperatures um and then comes back with his recommendation right and you
2:49:23
go okay show me the minor report yeah show me the the thinking how did you get
2:49:30
to that right exactly so but you'd be doing that would you be doing that inside of orange or inside of red um
2:49:38
well Orange has finished its job yeah um orange was meant to produce a report
2:49:43
yeah but these so keep in mind that these messages from Orange are VIs ible
2:49:49
to the user on the thread because orange wasn't working in drone mode orange was working
2:49:58
on thread yeah but it's the um it's the pop thing so um by pop what I'm assuming is
2:50:06
in the long thread orange is uh there's lots of work lots of work lots of work
2:50:11
yeah and then squishes it no the the output is
2:50:19
passed um back to the red one but the thread contains all these messages the
2:50:26
squishing doesn't the squishing happens far
2:50:32
back that is not squished so what what do you mean by pop then pop means
2:50:39
to when the orange b terminates or
2:50:45
recognizes the completion of its job which is tricky because you've got
2:50:52
to prompt it to know that it's going to get called in this terminal fashion when when that bot somehow or
2:51:00
rather signals that it's finished then switchboard
2:51:07
or some mechanism switches back the current agent to be red MH and gives it
2:51:16
a chance to carry on now that all of the orange messages are
2:51:22
on thread given that it switched to Orange in the first place to get a job done during by pop all you're doing is
2:51:29
who am I talking to now yeah who did I switch back to who who which agent was
2:51:35
previously the one I was talking to that agent doesn't have any of the uh CIS
2:51:40
prompt of the one that's just been popped back from it doesn't have the CIS promp but it's got all the messages it's
2:51:47
got all the messages that the previous agent did right um I think that would be
2:51:52
reasonable wouldn't it because so that that is that is long threading but this extra feature is
2:51:59
saying that previously we said there's an agent you talk to an agent a human
2:52:04
talks to an agent if the agent wants to get other AI tasks done it calls a drone and a drone is not allowed to talk to
2:52:12
the human but there is actually another case where the agent wants to
2:52:19
switch to another agent that is capable of talking to the human to get its job
2:52:25
done and to reduce ambiguity by way of conversation but it still has this
2:52:31
concept of it's there to do one job and then that job is done and it passes back the result to the calling agent in a
2:52:39
way and so that's what this is conceptually makes sense isn't it because essentially what you're saying
2:52:44
is um right uh I'm talking to uh Agent X uh
2:52:52
it's like okay right I need a more specialist agent y okay I'm not talking to you yeah re why we go backwards and
2:53:00
forwards whole bunch of stuff there it's like okay that's placed back into HX HX
2:53:06
still knows what your intent is yeah so that'll be like you're sitting in the office um you call in one expert for
2:53:14
whatever reason you're like uh what's the Square < TK of two to 57 decimal places
2:53:22
and then that agent goes uh oh I need to call my math nerde it switches in the
2:53:29
math nerde and then the math nerde is like um you know what base number did
2:53:35
you want that in uh BL like ask a bunch of other questions right and
2:53:41
then eventually calculates an answer based on that and then hands back to the
2:53:47
original guy and and all if it's ambiguous uh so
2:53:54
see if uh Master agent uh give me pi he
2:53:59
goes it's like no give me more Pi I like Pi it's like okay that's good enough you
2:54:06
go back so now you got two answers um but both answers are
2:54:11
available to the original thread that's right the original thread has all the messages and that includes the ability
2:54:18
to deduce that the first pie wasn't enough you wanted more and so that's now
2:54:25
even you can choose oh all right
2:54:30
uh I'm got a call from the United States why I'm getting call um so uh yeah so get both answers
2:54:39
back and then it'll make its best judgment if you say right okay so uh you
2:54:45
know tell me what rot pie is uh it'll make a fres yeah you go then
2:54:50
you can also say h give me two more Precision it's like ah I've got another
2:54:56
answer yeah yeah that that makes sense that
2:55:01
that feels good okays good so I'll Implement that into it's
2:55:07
just yeah I I think we're getting closer and closer to a stable
2:55:12
model these are all just little nuances that only really appear once you get into the into the weeds of it and the
2:55:20
testing framework is key to being able to exercise these kinds of systems and make sure they behave how we want very
2:55:27
much so very much so and um yeah the
2:55:33
uh feels like um back chat is probably got still a rule um but as
2:55:42
almost like a running task that the uh M can call on if you're asking for
2:55:49
just Brute Force do stuff what would that be um like uh okay
2:55:59
um I've just calculated or you know my agent just calculated two pies I'd like
2:56:05
to save those into two different files please that wouldn't really be back chat
2:56:12
though would it that would be um the files agent I would
2:56:19
imagine yeah but backat is a combination of all the power operations that
2:56:25
interact with Git well all of the agents many of the agents have the
2:56:31
ability to interact with Git like the meeting bot was able to read from git
2:56:36
and do some stuff I just I think what you're really meaning is you want like a system or
2:56:42
file system level thing and you've attached that meaning to back chat but
2:56:48
yeah I think it feels like it feels like just another bot really it's just yeah I think bechat dies now it's it's it's a
2:56:56
cool concept it's a cool name but I think that it's yeah I know I know and I named so
2:57:03
many things in the code repo back chat so that's annoying but
2:57:09
um so m m takes over the Summoner and does the switching
2:57:16
between threads yeah and switchboard creates new threads
2:57:22
and makes them um makes M aware of those threads well
2:57:27
switchboard there's always a base thread and if M can't handle it then it goes to
2:57:34
the base thread which is what back chat used to be That's That Base thread is backchat I
2:57:43
think uh well previously at the start of the call we were talking about how doing that yeah but how so how on that on that
2:57:53
thread that background thread that primary thread there are a number of agents that are presented to you in the
2:58:00
in the vanilla form one of those agents is hell and like that's the thread that you
2:58:09
know that's the system we present and then people can use it to switch over to
2:58:15
a CRM thread after they've logged in for example I think that makes sense I think that
2:58:20
makes sense and so how how is just an agent another agent on that on that
2:58:25
background base thread and that's why I think it's it's back chat in
2:58:32
principle but it either needs a new name or in
2:58:38
honor of backchat we can keep it the same or whatever but the back chat is is
2:58:43
the first of all there's no need for a keyword for back chat anymore because we use meaning yeah um good yeah and back
2:58:52
chat could just be the the root the the name that we give to the root chat or the first thread so if you make a new
2:59:00
tab it'll make a new back chat and then in that session you you know there's an I don't
2:59:08
think that's necessary well that that's with the model um the uh or something in St
2:59:17
sheets uh switchboard instantiates yeah uh instantiates what
2:59:24
um how for example well there needs to be a thread first and then um
2:59:32
switchboard chooses to direct the user's input to hell yeah but I'm thinking an
2:59:38
absolute clean uh situation where you turn up nothing's happened nothing's happened I have made you a thread by
2:59:46
default and switch switchboard is there and active and switchboard you haven't
2:59:53
said anything so switchboard hasn't chosen anything yet and it waits for your first that dread that that feels
3:00:00
like how right it's your but how's an agent on it agents on it hell is an
3:00:05
agent on it um do you want to do you want to name
3:00:12
Howell is the complete system of multiple agents I'm thinking um when you
3:00:17
turn up and you've never used this thing before um having something that actually
3:00:22
uh spends time with you has fun with you talks about a
3:00:28
lotos the power of that system is knowing when to switch agents depending
3:00:34
on your interest and so right yeah and so how is just one of the agents yeah um
3:00:41
maybe I'm getting a bit sentimental here um but how seems to be your guy the go
3:00:47
he the default bot like if if you say something and M's like I don't have a thread for that okay I'm going to the
3:00:54
main thread and then you land on the main thread and switchboard is like oh I don't know what the hell this guy's
3:00:59
talking about that's when hell gets called H is the default the default agent for the base thread right if you
3:01:08
go back up um the rabbit holes all the way the last thing you're going to see is how it's like thank God you're here
3:01:15
okay if you yeah right if you've exhausted all your rather reasonable options how appears yeah but there needs
3:01:22
to be something instantiates how which is the kind of boot bootstrap that's artifact artifact kicks that all
3:01:30
offact yeah okay good okay right um don't think back chat has a particular
3:01:36
role here oh sentimental all right so back chat's dead I think so I think so
3:01:43
this well let me stick into meeting part and yeah think about it sounds it sounds
3:01:48
like it's unne it sounds like back's dead yeah yeah right uh just the time I
3:01:54
need to go man all right to probably definitely need if you don't want to call it back chat then I do need a name
3:02:00
for what this base thread is because base thread is
3:02:06
unspecific can we call it well why not
3:02:14
uh I know in the architecture how is just another thread yeah but we're
3:02:20
talking about another agent it's like the um you know the first amongst
3:02:26
equals um there seems to be a uh if it's you want to call it hell is that what
3:02:32
you're going to say yeah yeah B if you go um you know up up up up up up up up
3:02:40
up you can go up again you talking to you're talking to hell I think they should be hell yeah you are talking to
3:02:46
hell but you want to name the whole thread as hell the whole black thread as
3:02:51
hell I do H's thread okay all right that's cool and uh I don't know I'll
3:03:00
just I I need to defer that rename for a bit cuz that's going to take a lot of time so I need to leave it named as back
3:03:06
chat for now and then I'll rename it to how later don't worry about renaming and send it um also I'm um there might be a
3:03:15
better way of talking about it because my we threw out as bit of
3:03:21
a name yeah true and it might not be the best but uh there is a name for that if
3:03:29
you go all the way up yep out of every Rabbit Hole you can you can't go any
3:03:35
further yep that thing that's what we're talking about yep
3:03:40
yeah right okay all right um cool I'll copy and
3:03:46
paste this uh meetings output over to you so you can have that for shits and giggles and then um nice yeah uh I am
3:03:55
I've got limited ability this afternoon being start the afternoon and
3:04:01
mentions but um on my side uh made quite
3:04:06
good progress I think especially with this uh this intest to be brilliant but
3:04:13
bringing in everything we've been talking about the last 6 months yep aw in order to to generate uh adjust Time
3:04:20
website awesome um and by that I mean you know here's uh 20 chunks of
3:04:27
text uh that depending on what you're interested in displays what you're interested in which seems reible that's
3:04:34
pretty damn good man yeah um and also uh as a throw side I've
3:04:40
already got a bot I'm not show you at the moment but just take my word on this um taking each one of these things and
3:04:47
cre a blog post right um uh well I was I was thinking more of
3:04:54
um uh I don't know what the right word is it's like uh today we talked about this a daily report summary um yeah it's
3:05:03
like yeah a log of what were we talking about anyway that's that's true sorry
3:05:09
that cool anyway got to go okay buddy uh that was deeply uh deeply enjoy
3:05:19
sweet I enjoyed that oh well plenty more to come I think
3:05:24
yeah okay I'll see you later talk you later okay see you bye

---