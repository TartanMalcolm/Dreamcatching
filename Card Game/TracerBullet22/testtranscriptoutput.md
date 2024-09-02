--- 
0:01 
- Tom: okay so from my side I want to present a um angle or reasoning
0:08 
- Tom: around removing back chat from being a
0:14 
- Tom: thing like um this thing uh I'm assuming that uh on the
0:20 
- Tom: right hand side I don't need to see any of that text Cu illegible uh that was the State Board yeah yeah no that's fine
0:27 
- Tom: but there's there's nothing specific in text doesn't matter it's the layout that's the thing and so back chat used
0:33 
- Tom: to pop up as a it would [Music]
0:42 
- Tom: um wait on back chat would do this right it
0:48 
- Tom: would come and go
0:54 
- Scott: yeah what yeah that is sloppy isn't it um
1:02 
- Scott: [ __ ] happen you uh what what are you doing there oh no it's G again this is
1:07 
- Scott: the slide it's it does this on purpose to show what happens okay so all right
1:12 
- Tom: okay right the user is using the thing back chat slides in back chat slides out all that now there's um two concepts
1:21 
- Tom: that I want to talk about number one is the user experience of what on Earth
1:26 
- Tom: happens if um I'm in this thread and then I want to
1:32 
- Tom: start talking to the CRM mhm and then and then I want to come back to
1:39 
- Tom: this thread so that's you know I don't think that I
1:45 
- Tom: should blank This Thread I think what I should do is let
1:51 
- Tom: you switch to this the CRM thread has to be
1:58 
- Tom: running in the CR repo it can't be in your repo because it needs to run under
2:04 
- Tom: the control of the application that's running it mhm right like it's got all
2:09 
- Tom: the Bots and all that and it can access parts of the repo that you yourself can't access but the thread can
2:14 
- Tom: communicate with it and all that a bunch of DRS and a bunch and then you also need to be able to let the owners of
2:21 
- Tom: that repo app see what everyone's done so you they need to see all the threads
2:27 
- Tom: of all the staff plus the staff need to see the threads too so that people can
2:32 
- Tom: see what's going on who did this why did they do that but you don't want to see
2:37 
- Tom: all their private chats that they were having all the other stuff and nor do
2:43 
- Tom: you want to make it so that when they're playing around in their own environment
2:49 
- Tom: and they call in a sketchy agent that's borderline
2:55 
- Tom: legit if it had access to all the data in the thread and the the thread contained all the CRM interactions then
3:02 
- Tom: you've now leaked the company info so you can't have that either and
3:08 
- Tom: so what I thought of doing is having the notion of a
3:16 
- Tom: um it's a thread it's sectioned threads and so it's sort of colorcoded or or
3:24 
- Tom: showing in the UI that somehow this portion of the message history
3:30 
- Tom: it belongs to belongs to this other
3:37 
- Tom: location so that when you're when you're in the enclosing
3:43 
- Tom: one uh I'm sorry I need to draw a picture I'm no I think you think going
3:51 
- Tom: from okay yeah yeah okay so you're like
3:56 
- Tom: message message message and this is you in your private space and then you
4:01 
- Tom: go hey I want to connect to the CRM and the system goes hokey doie and then your
4:08 
- Tom: messages show in a maybe a different color or just a different way to indicate that this portion is separate
4:17 
- Tom: from this portion and then somewhere down here you go hey I want to get out of here I want to go back to where I was
4:23 
- Tom: before and then it goes okay and you come back to this thread right right right right so you got layers but but
4:29 
- Tom: also um tricky part is uh for the blue stuff when you're doing let's call it
4:36 
- Tom: Agent X yeah um and uh so if you add in a few more blue layers underneath the
4:42 
- Tom: black at the bottom when Agent X is uh talking it's thread it's only the blue correct and
4:51 
- Tom: then when you're talking to agent black it's only the black that's right and now
4:56 
- Tom: blue doesn't need to see black for any reason well it it shouldn't
5:03 
- Tom: because no no no no yeah I knew this was I knew this was contentious but this is
5:09 
- Tom: my conclusion is that blue blue has no business knowing about
5:16 
- Tom: black whatsoever uh in this instance yes yeah
5:21 
- Scott: well in any instance because black is the parent and blue is the
5:27
- child um yes but the uh uh suby here or I think you probably
5:32 
- Scott: already thought about this uh subtlty is CRM might have um uh sub Bots inside of
5:39 
- Tom: that correct we should have different colors and you they would the Bots would change but
5:45 
- Tom: the thread would stay the same so like your your CRM thread in the the black lines the Bots
5:52 
- Tom: are switching in and out but they're your Bots with access to your data in the blue thread the Bots are switching
5:59 
- Tom: in and out but it's only the crm's data okay it's all right okay so let's
6:05 
- Tom: think about this um if you add in another color let's make it a bit more pruy um I in um a pink layer now is who
6:13 
- Tom: is who is pink a child of is pink a child of black or pink a child of blue
6:19 
- Scott: uh well let's see black is how right yeah black is the original you started and here you are and how's your friend
6:26 
- Scott: yep yeah um and then you've gone and done blue with CRM yeah then you gone
6:32 
- Scott: let's say back to Hal yeah um and then you're now in pink so I went back to how
6:38 
- Tom: and then I went I don't have a pink Red's going to have to do you I love that you wanted that color most of all
6:45 
- Tom: but anyway so oh sorry salmon salmon inside inside of a Sal inside of a
6:50 
- Tom: salmon the salmon internal internal Swatch hell um okay and then so that's
6:58 
- Tom: the the other thing like
7:04 
- Tom: uh maybe that's Bank just make it make it sort of seem important so now you've
7:11 
- Tom: got um three threads going um now I
7:17 
- Tom: assume um well does black know about the
7:22
- whole Shang I think that black I think that black knows about the whole shebang
7:29 
- Tom: but black black cannot see inside it so black would get like a summary of what
7:34
- Tom: happened so that when you're in Black you're like hey remember when I was talking to the CRM and I said blah blah
7:40
- Tom: blah blah blah um what what was that about again so that you
7:46 
- Tom: can uh no that's the um well given your uh emphasis on uh
7:53
- Tom: leakage uh what you'd want to do is um black uh doesn't know anything about
8:00 
- Tom: I think that I think that like it's okay for black to see completely inside the
8:05
- CRM the thing that's not okay is for black to switch to an agent that isn't
8:12
- trusted and then also allow full visibility into the thread so another
8:18
- way that we could the second one of I absolutely agree with yeah the second way we could have handle this is to say
8:25 
- Tom: that black is special in that it's only certified safe Bots and in which case it would be okay
8:33
- Tom: to let black see the whole thread
8:39 
- Tom: verbatim yeah because if if the user saw the thread then it's okay for the user's
8:44
- Tom: agent to see the thread so long as the agent is trusted another way of doing it possibly is um black knows that you've been talking to you know this hussy CRM
8:57 
- Tom: B yeah yeah um and as soon as you ask about a question about the CRM bot
9:03 
- Tom: you're you're now talking uh to the CRM bot so there's a difference between thread and display
9:10 
- Tom: right we can display it yeah I just didn't want to I just didn't want to
9:15 
- Tom: um end up in a position where I'm showing the user one thing and then the
9:21
- Tom: user tries to talk about it or select it because I want to make the messages
9:27
- Tom: selectable like so I can pick this one and talk about
9:33
- Tom: it well the question is who you talking to so say if for example CRM had its
9:41
- Tom: own uh long thread it's version of how how CM yeah yeah that's right um and so
9:49
- Tom: uh all your um your black uh how just knows right you're talking about the CRM
9:56
- Tom: now I'm just going to pass you to the CRM now the question is would you ever
10:01
- Tom: want to um have any kind of conversation about uh red and blue while talking to
10:09
- Tom: Black it's like black blue it's not it's sort of yes yes you might you might
10:16
- Tom: because if we're going to present them all together then of course at some
10:22
- Tom: point someone will want to have a multi-threaded conversation now the other option is
10:28
- Tom: to uh switch out the whole thread so that when you talk to the CRM it's a
10:33
- Tom: blank thread and you're just only seeing that data right and then when you switch
10:39
- Tom: back do as essentially a new H it looks like a new H yeah only is only on they
10:45
- Tom: can do all those yeah yeah yeah and so we would indicate to you using a lozenge
10:50
- Tom: of some kind that um which which what the location of your thread
10:58
- Tom: was so for example that little lozen there might change to to help tell you
11:04
- Tom: where where you are like are you talking to your H or are you talking to the
11:10
- Tom: CRM um all those kinds of things right so really is just an
11:15
- Tom: interesting one okay so uh I love my analogy so here's an analogy right you've got
11:22
- Tom: uh uh the user is a double agent talking to uh the Soviets and NATO at the same
11:28
- Tom: time right uh you don't want you want the uh the user in this
11:36
- Tom: case the double agent to be able to do that you don't want nle ever to know anything about the Soviets you don't
11:42
- Tom: want the Soviets ever to know anything about correct okay well it sounds pretty
11:48
- Tom: obvious then that what you're advocating for is that when I whenever I switch
11:55
- Tom: threads the whole display resets it sounds like it it sounds like when
12:01
- Tom: you um call up the CRM then you get a new how okay now the the thing we
12:07
- Tom: could add to that possibly is allow uh so we were talking about um the top
12:13
- Tom: level black uh how yeah knows that you're talking to the CRM just doesn't know what you're talking
11:13
- Tom: about um it could it it could and maybe it should but I think that um if we
12:28
- Tom: separ at the visual presentation it makes
12:34
- Tom: it so that you can't be talking to
12:40
- Tom: red and you can't talk to Red about blue or you can't talk to Red about black but
12:47
- Tom: you can talk to black about red and blue yeah but here's here's the thing right so you're in black and you've been
12:54
- Tom: talking black knows you've been talking to blue and red yeah um you ask a
12:59
- Tom: question in Black uh that is actually the business of
13:05
- Tom: blue um and it passes on the question to this the uh blue and the blue can decide
13:10
- Tom: whether to answer or not it's like so you want that that's the like the knowledge Realms of each black says all
13:19
- Tom: red says only red blue says only blue uh no no uh if you were to uh so let me let
13:26
- Tom: me think through this so and this is probably not right but that's go be so you're in
13:32
- Tom: Black uh talk to Blue talk to black talk to Red talk to black okay then black
13:38
- Tom: he's saying right uh blue is um generated this file I went red to know
13:46
- Tom: about it uh should be able to ask blue but blue has its own permissions blue no
13:54
- Tom: no no black isn't black
13:59
- Tom: has the power like all all the conversations with blue actually under
14:05
- Tom: the hood go through black because black is the users terminal thread and so it's
14:12
- Tom: it's like if you SSH into another terminal even though you're securely
14:19
- Tom: connected and this thing's got permissions up the wazu all your keystrokes are still going through your
14:25
- Tom: original terminal to get there yeah um yeah uh that's quite good anation so so
14:31
- Tom: if I want to do the file transfer what I would do is I would have to say uh black
14:36
- Tom: reach into blue and grab me this file and it would be like okay cuz I've got the history and then once I've got it I
14:44
- Tom: would oh that's R the wrong way but you know what I mean and then I'd put it into red right you've now got some weird
14:51
- Tom: kind of character here it looks like it's crying yeah it is that's how I feel every day working with these problems I
14:58
- Tom: would I would um uh I would add a bit onto that uh in that narrative uh black
15:06
- Tom: uh says blue you've got this file I've just been told you got this file give me
15:11
- Tom: the file blue should be able to under it own permission say no you're not getting that file well yeah yeah yeah yeah
15:19
- Tom: absolutely but if you
15:26
- Tom: hadn't yes um but that's no different to being in blue
15:34
- Tom: and you you wouldn't have access to that file anyway anything that anything that
15:40
- Tom: blue lets you access black therefore has access to but of all the files in the
15:47
- Tom: CRM your thread within the CRM may be denied access to some because of who
15:53
- Tom: black is because black is your identity and you converse with the CRM as black
15:59
- Tom: within the black thread and that's why if if the CRM thread lets you see a file
16:06
- Tom: black can see that file so it's a bit like having uh two servers and laptop
16:12
- Tom: and uh two servers individually have their own permissions correct but your laptop has permissions to into both yeah
16:20
- Tom: yeah so I do an SCP on one yep now got it yeah and it would come but it would
16:25
- Tom: have to come through your laptop to the other server right and so the permissions um are uh if you were to try
16:33
- Tom: and SCP a file which um blue didn't allow you to have a black yeah going say
16:39
- Tom: you get to that yeah yeah that's right yeah that makes and then Additionally
16:44
- Tom: you may the system may allow red and blue to
16:49
- Tom: communicate independently of black anyway so you know that that's allowed
16:56
- Tom: too I just want to make that point yeah yeah um well that would be uh blue and
17:02
- Tom: red would uh inherit the permissions of black saying can you guys can we talk
17:09
- Tom: it's like yeah yeah we can talk oh right so like um black could give them permission to talk to each other on
17:15
- Tom: behalf of black right because ultimately black has the permissions of the user is
17:20
- Tom: correct effectively is the the user yep okay awesome okay so that settles that then
17:27
- Tom: we will when you when you dial in when you first start up you get the black
17:33
- Tom: thread which is your how and then you say I want to work on the CRM and it
17:39
- Tom: does the login and all that stuff and then it resets the message thread
17:45
- Tom: because you're looking at uh a dedicated new thread that's running over here on the
17:51
- Tom: CRM yep but all your messages are still going through black under the hood they
17:57
- Tom: just don't show up as um they don't show up in the message
18:02
- Tom: history of black because you're now talking to this new dedicated thread yeah now when you thr up when new thread
18:09
- Tom: uh and in blue for example um and then red uh you don't want is accidental
18:16
- Tom: leakage um so every all the information is in Black by the fact that you can access blue and red that means you have
18:23
- Tom: permissions correct um so is there any way that
18:29
- Tom: information could leak between blue and red in that situation not exp not at all yeah so um the other
18:37
- Tom: thing is that um I want to switch I want to remove
18:45
- Tom: back chat from being a thread to being
18:51
- Tom: an agent within hell and so I think that I still want to have the
18:00
- Tom: Summoner um and I'll try and draw a picture here because when I've explained
18:06
- Tom: this to you in the past and then I listened to my explanation I was unimpressed so the message all
18:14
- Tom: messages under the hood come into black in terms of like this is
18:21
- Tom: your uh your terminal where it comes in by messages do you mean prompts prompts yeah from
18:28
- Tom: the user saying anything first goes to here then it's going to go to
18:35
- Tom: the I think it goes to the Summoner where it says
18:43
- Tom: um draw the Summoner in green and the Summoner says did the user want to keep talking
18:51
- Tom: to the thread that they're in or did they want to jump out and talk to the
18:56
- Tom: containing thread or some other thread in the stack so I want to int the cont
20:03
- Tom: switch right yeah I want to introduce the concept of a stack and a a thread stack is like I could be say I'm in red
20:11
- Tom: and then I I cause the Summoner to get me out of here like I'm like help please
20:18
- Tom: help I want to stop talking to the bank I they want to take my house and then
20:24
- Tom: the Summoner intercepts it doesn't send it to the bank drops you back to black
20:30
- Tom: because that's the most appropriate thread that it thought you wanted to be in right
20:36
- Tom: then you go I want to talk to this other thread which is the orange thread don't
20:42
- Tom: know what it does maybe it does juice cuz it's lunchtime then when you're in the orange thread you
20:49
- Tom: say I want to talk to the salmon thread but that's now you didn't go oh what the
20:58
- Tom: fluff let see what you're saying right here we go the purple pimper nickel and then it
21:06
- Tom: goes to this other thread but this the stack has
21:12
- Tom: gone um oh dear oh dear my artistic expression is
21:19
- Tom: lacking um goes there and in this case the stack still contains orange and then it
21:27
- Tom: contains pimp in the because
21:32
- Tom: the when I when I hit the Summoner and I'm like oh Summoner get me out of
21:37
- Tom: here um it knows the thread stack because let's say this was called
21:45
- Tom: the the juice bar and this was called the the allergens bot cuz I was going to
21:52
- Tom: order a fancy sort of a smoothie but I was like it's got monk fruit in it I've
21:57
- Tom: never heard of that in my illus to it it be me yeah yeah and then I could go H
22:03
- Tom: Summoner get me I could go summon I want to talk about holidays and holiday and
22:08
- Tom: summon is like oh that's okay I'm going to drop you back to hell because that's got nothing to do
22:14
- Tom: with anything on the stack that sounds a lot like backat though but hang
22:20
- Tom: on it's it never back chat used to have some functionality the Summoner is only
22:28
- Tom: for switching you between threads now the Summoner used to switch you between
22:36
- Tom: either back chat or the current thread Now it only chooses
22:41
- Tom: between which threads are currently open before there were only over two threads
22:46
- Tom: open now I'm saying we could have it could be stacked arbitrarily deep and suon it can switch you between
22:54
- Tom: them right mhm okay and and and and
23:00
- Tom: history it's just sounds like a top level switch board yes but it doesn't switch between
23:07
- Tom: agents it switches between
23:12
- Tom: threads ah yes and so I could I could be down
23:20
- Tom: here talking about monk fruit allergies and I could say oh wait I want to go I
23:25
- Tom: want to go talk to the bank again and then summon a would drop you back
23:30
- Tom: into this thread here right so uh to pick up analogy from
23:37
- Tom: our last call um I was talking about uh you've got a very large seat and
23:43
- Tom: mahogany desk and one laptop and different number of people we can call on yeah and uh I'm working on this oh
23:50
- Tom: get yourself in here do that right go away next yeah uh or go away and you
23:57
- Tom: figure it out and come back okay so that is um one um pattern mhm the second
24:03
- Tom: pattern is uh I've got an infinite uh office and I'm walking around with uh no
24:11
- Tom: no I'm going into each office and there's a new laptop each time yeah that
24:18
- Tom: was our that was like several models ago for us yeah so that's interesting so
24:23
- Tom: we've got so that seems to be um well those those two models um
24:31
- Tom: seem to make sense right right but working on one thing or am I working on
24:36
- Tom: yeah yeah but so so originally we were walking around to each office right right then then we modified
24:45
- Tom: that to say um we want to switch the office uh sorry we want to
24:52
- Tom: switch the worker we want to stay in one office and we want to switch out the workers and now what I'm saying is that
24:58
- Tom: we want to be in one office switch out the workers and then switch office and
25:03
- Tom: then switch out workers there and then switch office again so it's like those two things
25:09
- Tom: combined yeah yeah yeah exactly or um it's uh one extends the other because uh
25:15
- Tom: being able to switch offices um reduces you back to ignoring the previous office
25:22
- Tom: state right but but the difference being that these
25:27
- Tom: offices can act as um conceptual isolation barriers but
25:33
- Tom: primarily they would act as permissions barriers so when you're like when you go
25:40
- Tom: to the bank the bank will switch out agents in front of you based on your
25:45
- Tom: request but you're at the bank it's not you're at the juice bar the juice bar agent would never appear behind the
25:52
- Tom: counter at the bank the bank would switch out its agent right yeah yeah
25:56
- Tom: you're going for like a you know you want the guy behind the desk saying yeah ah would you like a lawn like yeah yeah yeah
25:59
- Tom: but when I'm but when I'm talking to the juice bar I should be able to pull in some info from a chat that I had with the bank um and I should be able to haul
26:06
- Tom: that in somehow well uh let's go with that analogy so the juice bar guy you're
26:23
- Tom: getting your juice from uh it says uh this juice uh cost about
26:29
- Tom: uh you know I don't have $1,000 um would you like a loan it's like well talk to
26:35
- Tom: my bank the juice guy calls the bank and the bank guy either says I can't that's
26:41
- Tom: yeah that's different that's that's independent of you that's got nothing to do with your frame of reference that's
26:48
- Tom: happening behind the scenes that's right but um there's no real difference between the user and Bot or than that's
26:56
- Tom: there is there is because the the if the juice bar rang up the bank the bank would probably be like who the who the
27:02
- Tom: fluff are you I don't know no there but the only difference is permissions right the juice bar phones up the bank says
27:07
- Tom: I'm not telling you that yeah and then you hand the phone and it's like yeah yeah yeah I've going through all the identification thing it's like oh yeah
27:14
- Tom: you hand the you hand the phone over yeah it's sort of like that so I don't know I don't know how to do
27:22
- Tom: that um it's almost it's almost like you want to call the Summoner or chat and be
27:29
- Tom: like hey can you pull in that info from that other chat and then drop it in here
27:35
- Tom: but then that starts to make backchat be a dedicated thread
27:44
- Tom: again you know you kind of want to be like uh drop me out you you kind of want
27:50
- Tom: to make it two moves like you're in the juice bar you go Summoner drop me back
27:55
- Tom: drop me back to hell then in how you're like uh grab the info from the bank okay
27:01
- Tom: and then you're like okay uh take that with me into the juice
27:07
- Tom: bar yeah but the two moves um I mean why aren't there extra moves life it's like
27:14
- Tom: uh [ __ ] that's an expensive smoothie right let me call a bank right Bank yeah
27:19
- Tom: but that would be a context switch for you you're in you're in the Smoothie Bar you'd you'd halt your interaction with
27:25
- Tom: the Smoothie Bar and you'd communicate with the Bank somehow you wouldn't get
27:30
- Tom: the Smoothie Bar to call the bank for you the Smoothie Bar doesn't actually inter yeah the Smoothie Bar doesn't know
27:36
- Tom: who your bank they also don't want to deal with it they don't make any they're like what the [ __ ] dude call my bank
27:42
- Tom: it's like you call your yeah you call your bank I'm not i' got smoothies to make you know yeah um okay so that's
27:50
- Tom: that's the uh the kind of can I can I can I chart that up as a a bit of a kink
27:56
- Tom: that I don't know how to solve it but we'll just play with it I still don't understand yes uh so I'm happy with this
27:03
- Tom: one but I still don't I get why we need to kill backchat because backchat is
27:09
- Tom: back becomes an a special thread that interacts with artifact right well
27:16
- Tom: backchat was a special thread that was the highest level thread because it
27:21
- Tom: could navigate you around through different threads and now what I'm saying is that there's only
27:28
- Tom: this this black thread takes on the role of what back chat used to be and so you
27:35
- Tom: never actually you you know you never actually relieve it why not if suar is basically
27:44
- Tom: the one who um understands the context switch the thread switch a thread switch is not a context switch it's it's bigger
27:50
- Tom: no the third switch is okay we're going to do this now but uh the Summoner something needs to say um okay so you
27:55
- Tom: just said take me to you know this yourm yeah let make it simple yeah um now the
28:02
- Tom: tech me to the CRM needs to be interpreted by a bot correct um and that is a context
28:07
- Tom: switch previously talking about Ro and Josh now I'm talking about CRM Su goes context switch right
28:12
- Tom: gotcha okay what you want is this right I think that the Summoner then
28:16
- Tom: um exists on this top level thread so that you when you're like why did you
28:23
- Tom: put me in this spot it would actually be a conversation
28:31
- Tom: in the top level because the top level would show why it you could drill down into
28:34
- Tom: why it switched you to whichever thread it did and you could see in your chat
28:40
- Tom: history your thread switches and then when you go click on them or talk about
28:46
- Tom: them it'll take you to that thread in a way yep y yeah with that sounds a lot
28:51
- Tom: like sorry bit yet um if
28:57
- Tom: I excuse me excuse me with what I'm about to
29:03
- Tom: doing by if I do that and now this is now totally independent but I replace it
29:09
- Tom: with some sort of a special looking message
29:16
- Tom: if I that would indicate you know uh switch to CRM
29:22
- Tom: thread when I click on that select it or otherwise tell using my voice that I
29:29
- Tom: want to talk about that thread yeah it will show the message history of that
29:35
- Tom: thread in the stateboard yes how's that yes that's
29:41
- Tom: good right yeah yeah yeah yeah exactly so so it'll make a widget that'll be
29:46
- Tom: specially it'll be unmistakable that you're looking at a windowed view right
29:52
- Tom: it's like now I'm talking to my bank it's like it's like this is a window into the conversation of the bank but
29:59
- Tom: you are not talking to the bank at this point you're just looking at what you said to the bank exactly and you've got
30:05
- Tom: like a notebook of everything you said to the bank you got a notebook everything said to the just bar I was
30:12
- Tom: like right okay going to the Bank notebook here uh the bank knows nothing
30:18
- Tom: about the juice bar juice bar knows nothing about the bank um how as your autor ego yeah knows
30:24
- Tom: that you got two notebooks and Sumer sounds a lot like a
30:30
- Tom: so that's um okay that mechanism there is how you
30:36
- Tom: could do the um transferring information from your bank conversation to your
30:42
- Tom: juice conversation because you would select the bank conversation while you're in
30:48
- Tom: Hell or yeah while you're in hell you would select the bank conversation and then you would say um bring the bank
30:56
- Tom: balance info over to my juice conversation and the Summoner or the switchboard or whatever it's become now
31:03
- Tom: would know that it would first of all have that data and then it would know that you want to now go into right right
31:10
- Tom: which sounds a lot like a credit card transaction right when you sweap your card to the juice bar uh the juice bar
31:16
- Tom: knows nothing about your bank right uh it goes off and uh goes through whatever
31:22
- Tom: you know Swift or whatever Network and all it comes back with is yes go for it
31:29
- Tom: doesn't know anything else but all the juice wants to know is do you have $1,000 to pay for right yeah right okay
31:38
- Tom: okay okay y so in that scenario you're treating the credit card as a piece of information that's authorized by the
31:45
- Tom: bank that proves to the juice bar that exactly but the justar had for example
31:53
- Tom: um uh asked the bank uh give me all your personal information of this guy and
31:58
- Tom: they go no [ __ ] off not doing that just come back with no you don't
32:06
- Tom: get okay all right so to recap you're only ever able to see one
32:12
- Tom: thread at a time when you switch to a remote thread like a conversation with
32:18
- Tom: the CRM or or with the bank um that looks like a whole new
32:24
- Tom: thread to you there's a stack of threads that is uh handled
32:32
- Tom: by it's not the switchboard it's the thing that switches you between
32:38
- Tom: threads um that that will always interpret your messages and determine
32:44
- Tom: whether or not you were talking to the Summoner itself or some other thread and
32:49
- Tom: it will always toggle you around between those and the Summoner actions happen on
32:55
- Tom: your base thread which is this original how the black it sounds about right
32:59
- Tom: name it for me what's the what's the Summoner name well before we go into the naming thing uh let me get this right
33:07
- Tom: because we've got two modes of operation here isn't it it's like um uh uh I've only ever talked to Black
33:15
- Tom: in this thread um now I want to talk to CRM right that was a switchboard thing
33:21
- Tom: so now no that's not a switchboard the switchboard as we had defined it before was switching between agents in the same
33:31
- Tom: thread right so who does that switch it's like I haven't talked to that's
33:36
- Tom: what I'm asking you to name it's I had called it the Summoner because the Summoner the Summoner
33:42
- Tom: handled determining whether you were talking to back chat the thread or the current thread that you're focused on so
33:50
- Tom: the Summoner is the one who invokes and instantiates new thread that you haven't
33:55
- Tom: talked to before correct okay the instantiator were kind of cool
34:03
- Tom: uh we give it a pistol well it might not be it might it might send you
34:09
- Tom: to a an instantiator agent because how
34:15
- Tom: you instantiate a new remote thread would be different for the CRM as it
34:20
- Tom: would be for the bank so it might be a convoluted process and the Summoner
34:26
- Tom: can't possibly know that process in advance but it could know how to send
34:32
- Tom: you to an agent that could figure that out for you H okay I've got an idea
34:39
- Tom: uh what's what's the name with the uh the top level I think Judy Den last time in the Bond films she was the one who's like sending agents it's like do this
34:50
- Tom: M so that's is that M yeah yeah but it's not you're not
34:55
- Tom: switching between agents you're switching
34:59
- Tom: between whole groups of Agents like MI6 CIA talk to the CIA talk to the
35:05
- Tom: Bolivian government right right exactly and there's a whole bunch of stuff underneath that and there's a local agent okay well m m works for me buddy
35:12
- Tom: I'm cool with that that's a that's a novel way to describe it interesting enough we also get for free Q for the
35:19
- Tom: tools but anyway uh might be a bit too
35:25
- Tom: much okay we we'll save that for
35:31
- Tom: later um m
35:37
- Tom: m extra large
35:43
- Tom: so okay all right so now a message comes in
35:51
- Tom: from the user a a piece of text comes in from the users hitting enter in the keyboard it
35:56
- Tom: comes into the backend terminal this is like the this is not an AI agent this is mechanical it's pass the
36:02
- Tom: authentication yeah this artifact level artifact then passes it to its first AI
36:10
- Tom: interaction which is with the agent M Agent M is special and that m is an
36:13
- Tom: agent that runs on the base thread but M gets everything
36:19
- Tom: first and then m is aware of all of the threads that are
36:24
- Tom: currently uh that have been active mhm
36:27
- Tom: um with some window and then depending on how M interprets that you
36:36
- Tom: will you will be your page you will change and you will end up
36:41
- Tom: in a different thread right does m uh save all those threads we've got one in
36:47
- Tom: I don't know is China whatever does m get to say right we need to go to to uh buen we haven't talked to buen yet what happens at that point that
36:57
- Tom: would drop you back to the base thread which is
37:01
- Tom: how and then how would use the switchboard to
37:06
- Tom: pick the appropriate agent to do what you wanted who's talking so m is talking to
37:14
- Tom: how no M does not talk M only Rel days okay so um IM switches how is how
37:23
- Tom: does how know about when is AR how doesn't but how has the agents that it
37:29
- Tom: uses when it doesn't know things so m is a right we've got four well let's go with this analogy because it's quite fun we got four operations going and five this doesn't five because you've always got home base so m is based at MI6 and these other threads are like the CIA MI5 CIA um all these different things yeah and now um M uh gets a
37:44
- Tom: request in saying we don't have any uh operations going at the moment covers this and it says how create me a new create this guy a new operation in
37:59
- Tom: Planet series one more time please so um uh in
38:07
- Tom: the analogy so uh M gets a request in looks through right we've got something
38:15
- Tom: in Moscow Tel Aviv Beijing and Washington y we don't have anything in W
38:29
- Tom: are yep uh so um M then says we don't
38:34
- Tom: have anything in Ben throw up an operation in Ben no M
38:38
- Tom: says Hey hell over to you all right so I can't do
38:43
- Tom: this you do M says we have no active operations based on this request how
38:51
- Tom: sort it out right right and how uh diligent dude that he is goes to right
38:58
- Tom: switchboard get me when series wherever the MI6 yeah get me the search function
39:06
- Tom: uh get me the web browsing function get me all these other things and then how works with the user to figure out what
39:12
- Tom: the user meant right and then now we''ve uh see we now I've got an operation in
39:20
- Tom: vaner that thread and goes oh brilliant I've got an extra operation here
39:26
- Tom: yeah okay all rights to work okay um
39:31
- Tom: could be a little bit jarring on the viewer though cuz if I'm
39:36
- Tom: if I'm looking at this thread um if I'm looking at one thread and then I get switched over to
39:42
- Tom: something else this screen going to just sort of drop away and then this new
39:46
- Tom: screen's going to pop up with this new thread is that
39:52
- Tom: okay should be okay right it is quite Jing I don't until we use it just like
39:59
- Tom: yeah we'll have to why don't we just see right cuz logically it makes sense yeah I don't want to have other widgets like
40:06
- Tom: listing your threads so you can manually select them thumnails yeah right it's like that we
40:12
- Tom: failed at that point um so like it it should be a big deal to
40:17
- Tom: switch operations because you shouldn't be dancing between them all the time you
40:22
- Tom: know like when you use the CRM you're [ __ ] you're using the CRM right now
40:27
- Tom: you can tell how to use the CRM on your behalf right so I think
40:34
- Tom: that's different be chatting to the CRM directly is very different to talking to
40:39
- Tom: and saying Hell you know how we're logged into the CRM I want you
40:44
- Tom: to use this bot that I just made to do all my work today go that's different
40:50
- Tom: that's you're still you're still talking to hell at that point but there's
40:55
- Tom: interactions happening with the CRM that could be populating the thread with the CRM too right but it's not how how is
41:02
- Tom: uh special because how inherits the Privileges of the user yeah yeah is
41:06
- Tom: the trusted the the sanctuary he's the inner sanctum of the user okay all right
41:12
- Tom: now so that's cool we'll deal with that and then we'll just I think it's faster to just do it and then see how it feels
41:18
- Tom: and then work with that okay so the next issue yeah sorry
41:24
- Tom: sorry yeah as a general thing throw out there it's much better to get the logic
41:32
- Tom: right because if the logic is right and it seems weird then that's training yeah
41:36
- Tom: uh or gooey yeah the logic be right the logic is the most important thing and I
41:42
- Tom: think if we just make the bare minimum interfaces for the logic so you're in
41:49
- Tom: agreeance with using the M using M as the thread
41:55
- Tom: switcher uh yes yep yes and then when you're in each thread they depending on
42:01
- Tom: how the thread has been configured keeping in mind that it's the vendor's Choice how to configure that thread um
42:07
- Tom: the thread may have a switchboard in place right and uh yeah uh just to uh do
42:14
- Tom: some Crossfire on this one um are two analogies of I'm working on my laptop in
42:19
- Tom: my uh office and I'm calling people in y That's a thread I'm moving to another
42:25
- Tom: office in my infinite office yep to work on this other thing that's the switch board thing right right right and just
42:32
- Tom: to understand that model you may you and I may go into the same office and look
42:39
- Tom: at the same laptop and we both collaborate on putting things in agents are being switched in and out to do our
42:45
- Tom: bidding and then I might be like got to go buddy and I go back to my office or some other office and carry on doing
42:51
- Tom: what I was doing there right yeah okay and
42:56
- Tom: finally I can also tell one of my agents in another office to act like me and
43:03
- Tom: talk to that office where you're in and you you wouldn't know whether it
43:09
- Tom: was genuine me or how acting on my behalf um well yes absolutely because uh
43:16
- Tom: the way be thinking about it is the user and how how is aoxy for yeah they look the same right in the whole ballpark
43:22
- Tom: they look the same okay so the next problem
43:25
- Tom: is well it's not nearly maybe it's a feature um is the concept
43:31
- Tom: of the concept of having a thread
43:38
- Tom: finish so uh wow this just like
43:44
- Tom: um let me try and let me if you just I I'll tell you a very different story
43:51
- Tom: I'll tell you a very different story about something that's that's equally useful but not related at all and then
43:56
- Tom: from that I hope I can show the problem okay so I made a thing that I
44:02
- Tom: was trying to get ready for you because I thought you would like it and then I ran out of time um what I've done oh man
44:08
- Tom: that's so sweet I think you I got you a cookie but I ate it um I copied your
44:15
- Tom: meeting bot mhm I put it in as an
44:20
- Tom: agent mhm I more or less copied it identically and then I gave it the YouTube fetch
44:26
- Tom: function which allows it to oh man pull in
44:31
- Tom: transcripts yeah um and I had as in a slide I hit an interesting bug that occu
44:37
- Tom: this is why I didn't finish it because I spent all of uh yesterday dealing with this bug where our our YouTube session
44:45
- Tom: previous to this one was Bloody long and when I did YouTube fetch the system
44:50
- Tom: crashed artifact crashed because the
44:56
- Tom: actions uh the way I'd built it because of limitations on the Deno KV store an
45:02
- Tom: action can't be more than 65 kiloby because actions are supposed to
45:09
- Tom: be regret that limit yeah no no that's not that's not true
45:16
- Tom: I when I store binary data or files There's No Limit because I use a library
45:22
- Tom: that breaks it up into 65k chunks okay but when I'm sending actions I don't do
45:30
- Tom: that and it occurred to me look I can either break up the actions so that they can be unlimited size but the choice
45:37
- Tom: that I've made that I want to run by you because it sounds contentious is I actually want to set the action limit it
45:44
- Tom: quite low because what in this case what
45:50
- Tom: should have done happened is that when YouTube fetch was called it should have the isolate that was running should not have returned the transcript as a
45:58
- Tom: reply to the request it should have written it to a file on artifact and
46:06
- Tom: then sent back the path to the file seems because it doesn't know that's doesn't know what you want to do with it no and so if you send it back what happens is it gets smacked straight into
46:12
- Tom: context now a lot of the time you want to do that but uh it's not I don't think
46:18
- Tom: it's a good pattern to do that by default because you've got no way like what if I what if the isolate wanted to return 5 gabes well interesting enough uh I've been this uh the uh prompt by saying um
46:32
- Tom: here's the file just say got it um and it doesn't go into the thread
46:38
- Tom: all you get in the thread is got it right but then it's uh it remembers it and can recall it and retrieve it and so on so
46:46
- Tom: yeah that makes sense to me that mirror is what I've been doing in uh in
46:51
- Tom: prom land okay so anyway that was a bug I so so you're okay if I set that action
46:57
- Tom: limit to be quite low because actions are supposed to be control instructions
47:03
- Tom: they are not supposed to be payloads in in my opinion they're not meant to be
47:09
- Tom: like binary data they're not meant to be big they're supposed to be instructions
47:15
- Tom: and for that yeah if if I've got this right um yes I agree in that uh now the
47:22
- Tom: size of instruction is something else but uh PE Lords being being dumped somewhere and then referenced back seems
47:30
- Tom: absolutely sensible okay great all right well let's what I have done let me just check
47:37
- Tom: that I [Music] um H where are we
48:01
- Tom: YouTube I want to say trust me this is worth it but um I don't know if it runs
48:08
- Tom: so it might not be worth it all right we roll family I I love a good far too
48:12
- Tom: early test I really
48:20
- Tom: do test tests sorry buddy I'm just going to oh
48:32
- Tom: you switch yeah I know cuz I I only want to
48:37
- Tom: run meeting bot
48:47
- Tom: okay okay it's good wait wait wait wait it's just running tests hang on it's
48:49
- Tom: gone and run oh cuz I got two ones my bad my bad sorry about that only only
48:57
- Tom: only you're the only one and so are you be only
49:08
- Tom: one which is completely obviously not
49:15
- Tom: right so we got this was the TPS
49:21
- Tom: report it ran one iteration it completed one in the test cases there was only one
49:27
- Tom: test case and it ran one it completed one and it had no success so it failed
49:37
- Tom: but the prompts this was the prompt that went
49:42
- Tom: in mhm and then it got back a whole lot of
49:46
- Tom: output which would have been [Music]
49:51
- Tom: oh it didn't read it [Music]
49:56
- Tom: into uh where does it say the output
50:08
- Tom: say it executed there it ran that with the
50:13
- Tom: prompt and then it said give me the transcript oh I know what's happened
50:21
- Tom: if if this is like dragging on too much you can definitely tell me but this is
50:28
- Tom: this is my this is my life this is what you I I'm cheting you're on here this is this is my
50:35
- Tom: this is my life this is what I have to do
50:38
- Tom: uh that's right so path was required
50:45
- Tom: and in meeting bot I need to tell it to give a
50:49
- Tom: path if you had to Fitch info from YouTube you
50:55
- Tom: will need [Music] to choose a
51:02
- Tom: suitable path to write the transcript
51:07
- Tom: to such as YouTube
51:16
- Tom: slash transcript underscore
51:23
- Tom: video ID I think that was it cuz I changed it
51:30
- Tom: to I had I had the YouTube isolate generating the file name but actually
51:35
- Tom: it's better if the meeting bot calls the uh YouTube function with doesn't know
51:42
- Tom: where what right yeah the meeting the meeting bot should choose the should
51:47
- Tom: choose the name
51:51
- Tom: yeah hopefully that worked but what oh
51:56
- Tom: dear didn't work now that was an open AI
52:06
- Tom: area oh I get those occasionally um quite often if you run it a few seconds
52:12
- Tom: later don't know what those guys are messing around under the hood or traffic or
52:17
- Tom: whatever that's weird yeah what these guys are doing
52:25
- Tom: let's see if hopefully an upgrade yeah yeah these guys are messing around with the under the hood but
52:30
- Tom: they're I think they're doing rapid like hourly updates or something like that
52:39
- Tom: uh it still asked for the transcript why is it asking for the
52:44
- Tom: transcript like it came back it called it as a drone and then its response
52:50
- Tom: was um please give me the transcript for the video but I I had it working before
52:57
- Tom: when the path was generated what did what did you put the point
53:02
- Tom: um you just move it you need to pistol whip it a bit like transcript is oh if if you put in
53:08
- Tom: if uh must always fetch a YouTube users
53:18
- Tom: will provide you with a transcript of a meeting or a YouTube url to Fitch the transcript from or a video D for YouTube
53:25
- Tom: video to F the transcript from okay that sounds reasonable right uh it does but I
53:32
- Tom: think you need to piss the whip a bit tell me what to do okay so what you got you got two options uh we provide you
53:39
- Tom: with the transcript um uh I assume that no transcript is
53:43
- Tom: going to be provided and fetched from YouTube If no YouTube uh is available
53:49
- Tom: then ask for a transcript
53:54
- Tom: that doesn't seem right because it seems like uh the reason why I'm pushing back
54:00
- Tom: on your is cuz this did work before the only difference is I've required it to
54:06
- Tom: choose the path that's the only change well the way to test it is um don't give an option um
54:12
- Tom: users will provide uh a URL so I think it's getting confused
54:17
- Tom: because it doesn't know where whether you're giving your transcript or URL and it's going yeah which one is it you are
54:23
- Tom: right you are right so can I try this and then if this doesn't work I'll try your thing yeah yeah
54:31
- Tom: okay but what I liked about this was being able to test that whole thing by
54:38
- Tom: just writing a markdown test file and going go like that's that I thought was
54:43
- Tom: pretty sweet it's nice H so that did work it called the
54:48
- Tom: thing but it um made it Absolut loot where it should
54:55
- Tom: be relative oh right okay which is a reasonable mistake to make a
55:01
- Tom: scoop and this is where I want to give you that ability to change the function
55:06
- Tom: definitions cuz I'm just changing it here like I'm changing it in the the API
55:12
- Tom: description which Alters The Prompt but I don't have a way to give you that at the moment so that's why I want to
55:19
- Tom: change that format to to let you modify that as part of your prompting process
55:25
- Tom: yeah cool well this is fun I feel like it's one way or another going to
55:31
- Tom: work oh wait wait wait wait what was that
55:36
- Tom: error path must be relative don't give me absolute path
55:42
- Tom: you scumbag how do I bash it into be be nice
55:48
- Tom: to it where are you talking about path relative path doesn't know what a relative path is um give it an example
55:56
- Tom: okay must end in. Json and must start with DOT
56:04
- Tom: slash how about that yeah be nice to it first time you've ever said
56:10
- Tom: that in like the last year that we've been dealing with this [ __ ] I've never
56:16
- Tom: heard that so this is your life right
56:24
- Tom: twiddling around with the oh yeah yeah yeah yeah exactly it's uh win nice witer
56:31
- Tom: pistol whop so we' we've definitely collided right like we're I'm doing your job and you're sort of doing mine yeah
56:39
- Tom: oh there's an error there what was that error no no error where's where's the ah it uh the test fail if I use only
56:45
- Tom: because there's like other tests that should have run two all right okay that's all so this was the output of the
56:53
- Tom: test case um that was the prompt and it still scored to
56:59
- Tom: zero um here's the reasoning
57:07
- Tom: oh this is message was a request for the transcripts not defend for conclusion or
57:13
- Tom: analysis of video okay so the output
57:25
- Tom: was so it fited the
57:30
- Tom: transcript and then it said oh please give me the trans [ __ ]
57:35
- Tom: sake this is is this your life this is what this is what you hate okay oh yeah
57:41
- Tom: yeah yeah yeah uh okay so it's saying please give me um why does it not think it's got the
57:47
- Tom: trans I got it I got it once the function has returned use
57:56
- Tom: the files read function to read the
58:01
- Tom: transcript from the path you gave the
58:07
- Tom: YouTube Fitch function it didn't know to read it back
58:14
- Tom: in it definitely called The Fitch but it didn't know to read it back in so this
58:21
- Tom: is like I'd imagine that this step that I'm doing here would be running in the
58:26
- Tom: browser for you where it's the tests um kicking off after you've twiddled the bot yeah
58:33
- Tom: and you get closer and closer yeah cuz there's uh some Nuance active
58:39
- Tom: voice really works right the users will provide you is a different
58:46
- Tom: and a much weak much more weak way of saying you will be provided by for
58:53
- Tom: example um it still came back and said please give me the transcript I need to tell it to read from the path that it just
58:59
- Tom: got okay you told up what the right okay so tell me through this so we it's
59:05
- Tom: already fetch the path it knows what the path is so it gener it generated the path and then it called the fetch function correctly
59:13
- Tom: um but then the function returns with just the description so should I uh
59:19
- Tom: yeah yeah um so give it uh a process um count this is
59:24
- Tom: Pudo code it's like um you will receive back X from X you to do
59:31
- Tom: y for
59:33
- Tom: doesn't know what a transcript is Ah that's a good
59:38
- Tom: point you said you will receive oh that's a great Point that's a great point
59:45
- Tom: you butt you you God damn it
59:51
- Tom: a path for the YouTube F function to write the transcript
59:57
- Tom: to.
60:00
- Tom: You will receive back a title and a description of the
60:07
- Tom: video uh but again you'll receive back a title and a description but no transcript like yeah
60:16
- Tom: yeah
60:19
- Tom: um how about that uh you still haven't told her what the transcript is okay
60:26
- Tom: where would I do that um okay so uh users will provide you with a transcript
60:32
- Tom: of a meeting you YouTube patch the transcript from
60:39
- Tom: video uh if you have to patch the transcript from the YouTube use the YouTube petch function you must choose
60:46
- Tom: path for the YouTube petch function to write the transcript to still haven't um
60:53
- Tom: said so what did you get back from that YouTube fetch uh it's a text
60:59
- Tom: uh a big long line of text that represents the transcribed version of the YouTube video so is it the actual
61:06
- Tom: transcription or um some kind of pointer to the
61:12
- Tom: transcription sorry uh so I I choose the path that I want to write the transcript
61:18
- Tom: to I then call the fetch function with that path the fetch function writes to that
61:24
- Tom: path and then when when I get back the the video title then I go read and get
61:30
- Tom: it in uh okay I think what I've done wrong is that it's confusing it by what I
61:36
- Tom: return from that function so why don't I just return um transcript downloaded and
61:43
- Tom: then give it back the path and then it will be like oh that's pretty [ __ ] obvious what I do with that yeah sounds
61:49
- Tom: like it should work okay this is this is frustrating and fun it is fun isn't it
61:56
- Tom: and yeah it's a lot like training a dog
62:01
- Tom: frustrating in a fun oh god look this is my
62:08
- Tom: mistake at the top level description of the function this is what I said see he's trying he's trying his best
62:15
- Tom: I know it's like you don't make sense like what do you mean I really want to please you what do you mean I a
62:20
- Tom: little AI span was trying to get all this fetched fetched fetch yes yes yes yes no that's WR or right like
62:29
- Tom: [Laughter] H you this will write the
62:37
- Tom: transcription Json object to the given
62:44
- Tom: path and [Music]
62:49
- Tom: return the title and description of the
62:56
- Tom: YouTube video oh God after matter yeah I think
63:01
- Tom: so um except for the uh spelling of transcription but uh
63:06
- Tom: yeah there's one mattera that uh realized is
63:11
- Tom: uh um doing all this really really really requires a lot of
63:16
- Tom: the human to actually be clear in yeah yeah and so making making a bot that
63:23
- Tom: could look at all that and then tell you and be like uh it sort of seems like you
63:30
- Tom: did something conflicting that's that's why I built how how three is like my my
63:36
- Tom: uh thinking is too messy you tell me what I've missed yeah um and a similar
63:42
- Tom: thing it easily be uh built um for this use case but it's
63:48
- Tom: amazing how much you how W you um [ __ ] up as a human I
63:53
- Tom: know one of my favorite ones we're talking about about one of my favorite ones is asking it say um what was asked
63:59
- Tom: or implied but never answered get this meeting that you've been in for an hour and everyone's going
64:05
- Tom: yeah yeah we know exactly what we're doing it's like Oh you talked about this and nobody said anything about it
64:10
- Tom: yeah someone asked this you never answered it
64:13
- Tom: um it's quite revealing how [ __ ] we are we are so [ __ ] we yes what's the
64:19
- Tom: funniest thing though is that we're so [ __ ] and unaware of it and so we don't think
64:25
- Tom: we're [ __ ] and you don't actually not like that whole time I was just like oh this bot's [ __ ] stupid what's going
64:30
- Tom: on but actually the my bad it always does something
64:36
- Tom: reasonable I think this is yeah this The Humbling thing it does exactly what you say know what you
64:38
- Tom: meant I'm going to get that my Tombstone I think what's that
64:43
- Tom: you're going to get a B right do exactly what you said but not what you
64:53
- Tom: meant okay and now I'm going to come back where I'm going to
64:59
- Tom: return um success is going to be a
65:05
- Tom: Boolean and then the path is going to
65:10
- Tom: be the path to the saved transcription
65:17
- Tom: file okay and now
65:25
- Tom: I'm glad that you're seeing me struggle like this cuz this is how my whole [ __ ] day goes this is my whole day
65:32
- Tom: but only recently has it become a bot prompting issue as well so that's sort of good that this is I'm I'm glad we're
65:39
- Tom: finally mashing in the middle you know um your uh your syntax
65:45
- Tom: and layout there I would be struggling with um but well as you can see I'm
65:52
- Tom: struggling with the bot prompting so that's
65:59
- Tom: good yes it did it this is the function call it was like it finally went files
66:06
- Tom: read and then here's the path be nice to the bot and the bot will be nice to you
66:11
- Tom: beest thou nicest to the bot and then what did it say and then it
66:18
- Tom: still said please give me the transcript it's in there hold on why why why um which uh in the flow here where is that um long for assistant
66:26
- Tom: agents meeting MD please give me the transcript up here what was the thing that was provided immediately prior the tool call where it read the um contents of this
66:33
- Tom: file right does it know that that path means a transcript well it called the tool
66:38
- Tom: it ran the tool the tool returned and then it said um assistant
66:45
- Tom: tool call read so it tried to read the transcript the transcript paths match
66:53
- Tom: exactly so it did a good job there it's got the um and then the
66:57
- Tom: content came back and it was like details title but then
67:00
- Tom: Subs is a key so it needs to maybe know that within that Json file it's got
67:06
- Tom: [Music] um Subs is the transcription Subs is the
67:11
- Tom: transcription I think is bit say okay right so St it um you recognize the
67:17
- Tom: transcript by the key Subs okay Christ am
67:23
- Tom: in so a bot that helped with this would be able to point out what you're doing
67:29
- Tom: right it's like right you know like exactly exactly it's like uh you haven't told it what what transcript is or the fact that Subs is the
67:39
- Tom: transcript CU it's not obvious that transcript equals Subs
67:44
- Tom: no I you know what I can do
67:49
- Tom: better I'll just rename the [ __ ] variable how about that
67:55
- Tom: how about that to how about transcript this is now going to be called
68:01
- Tom: therefore oops uh trans [ __ ]
68:06
- Tom: script here we go all right
68:10
- Tom: okay I have stick that in your button SM a warm feeling about this one but we'll
68:17
- Tom: see I've lost the ability to have warm feeling
68:23
- Tom: I think pretty early on in my coding career I realized that if I had to pray my code
68:29
- Tom: [Laughter]
68:32
- Tom: sucked oh it's still asked for give me the transcript give me the
68:36
- Tom: transcript so I should I should who's asking that at what point why are you
68:41
- Tom: asking that in the process you must call function
68:46
- Tom: to
68:50
- Tom: yeah uh yeah I'm what doing mistyped the first
68:55
- Tom: transcript although it's pretty good at M typing actually yeah it's pretty good
69:01
- Tom: okay how's that okay let's give that one Let's
69:07
- Tom: uh what are you doing oh God bot programming it would be
69:13
- Tom: so much easier if we had a bot to do this oh work on that one I'm really
69:21
- Tom: working on that how three is just like the start just a
69:28
- Tom: start okay you go please give me the transcript right okay so one a second
69:33
- Tom: what was so just above that if you go back just above the please give me the transcript what was so this is obviously
69:40
- Tom: a transcript this is all the J this is the Json object that came back
69:46
- Tom: yeah um gosh you do talk a lot right okay so that was a tool
69:51
- Tom: call and the assistant had asked to read this
69:56
- Tom: file I gave it back this file the content was [Music]
70:02
- Tom: um uh bracket
70:07
- Tom: details bracket descript
70:12
- Tom: close bracket transcrip
70:16
- Tom: the which one this one marks yeah this one uh because the quote marks need to
70:23
- Tom: be escaped because oh all right okay yeah yeah okay f um is it cuz it thinks
70:30
- Tom: transcript isn't the interesting thing is that this is all Tech there's no speaker identification there's no time stamps
70:38
- Tom: it's just one big long thread uh it might be thinking that transcript
70:45
- Tom: that it doesn't make sense to be a transcript um uh why not just dump the entire contents what of it uh and not
70:51
- Tom: call it a transcript oh well transcript is fine right but uh okay so you got two
70:58
- Tom: call that's giving all of all of this text yeah um if you were to like simp copy
71:06
- Tom: and paste that into a dumbo it would work out right it's like
71:12
- Tom: so what you're trying to do is uh strip out the transcript part and leave the details in the title that's right but that's fine you think it's confusing it you so I
71:21
- Tom: you just want me to return only this text yeah uh no no uh I um return um
71:27
- Tom: give it the entire contents what under content just give it give it all of it that's
71:35
- Tom: what it got this this content went back into the bot from from this point on everything
71:43
- Tom: got that's now context straight back into the Bots thread okay but the prompt
71:48
- Tom: is saying um get the transcript yeah uh from that um where it's uh get
71:54
- Tom: the um the contents of the file uh I'm I'm not withth you sorry I'm
71:56
- Tom: sorry um if
72:02
- Tom: if you go back to the uh The Prompt where uh it's like in the meeting bot
72:10
- Tom: okay so I see this access the transcript you must oh look look at that look at that example transcript
72:17
- Tom: format Ah that's my old format which just does not apply and
72:24
- Tom: then it's like well you didn't give me a transcript so right right oh good spot
72:32
- Tom: good spot okay well a bot would have got that right a bot would have got that EAS easy one is to cuz being
72:39
- Tom: giving an example is a nice thing but it's not necessary so strip it out run it see
72:46
- Tom: Happen strip this whole thing yep EXC me mate your cough sounds like
72:54
- Tom: mine oh I've been a bit ill heav you yeah just a virus don't [ __ ] die that a l will kill me one the two are we don't really care other people
73:01
- Tom: do some IR
73:06
- Tom: here man this is painful and fun still didn't
73:12
- Tom: work where did it fa
73:17
- Tom: did you uh strip strip out all the example from the
73:21
- Tom: meetings so I've got the
73:27
- Tom: um please give me the transcri please give me the transcript this one it's
73:33
- Tom: got a definition in its head so what's happening here is it thinks it knows what transcript is more writing
73:39
- Tom: and saying that's not a transcript you asked me for a transcript please give me the trans script so there's something
73:45
- Tom: around the definitions now examples are like proxy definitions is that I'm not
73:51
- Tom: going to Define it uh however here's an example and work it out so um if there's
73:57
- Tom: anything still meeting part that's an example that might be throwing off um the flip side of it is we could give it an example
74:04
- Tom: um and say you know here's what you're looking for this is what we mean by transcript but the um this is a
74:10
- Tom: definitions problem which is why i' be banging on about uh definitions uh example interactions no
74:17
- Tom: that's fine that's not talking about transcripts answer Y is there anything further
74:21
- Tom: down fine oh that look at
74:27
- Tom: that there is there is ah ah God
74:34
- Tom: okay trying poor bot there poor trying to do it he's just trying to do
74:38
- Tom: it it's so good right like it's just it's just it never ever does things that
74:45
- Tom: are unreasonable yeah like even when my buddy got called
74:51
- Tom: a [ __ ] he uses the word [ __ ] a lot and he's also very sarcastic so what he must
74:57
- Tom: have done is said I love being called a [ __ ] and then it got stored in memory and then the pot came back and was like
75:04
- Tom: enjoy your cocktail [ __ ] and they're saying don't C up Mor
75:09
- Tom: and then it goes back into dog right it was I'm so sorry I'm so sorry okay there you go buddy here it is
75:17
- Tom: right so we've yeah we passed the test there you
75:24
- Tom: go the assistant mention developing a comprehensive blah blah blah okay
75:31
- Tom: so what was the output here the output uh I'll just grab all that and
75:38
- Tom: put it into something nice and easy on the
75:47
- Tom: eye okay
75:56
- Tom: that is exactly why our testing first thing is important right and testing
76:04
- Tom: with variations as well on my ADD yeah yeah because
76:10
- Tom: um that would have been well it was what half an hour of trying to figure out the fact that
76:17
- Tom: we' actually told it to something that we didn't want to tell it yeah that's my bad cuz I just lazily copied and pasted
76:23
- Tom: all your stuff no but people are going to do that I know right it's a
76:29
- Tom: reasonable thing they want to do I just like I just want to get going like a can I use that but over here the video title
76:35
- Tom: outline there you go that seems uh pretty reasonable and uh
76:41
- Tom: in the in the running thread can you ask it questions or uh no because it just ran the test all
76:47
- Tom: right okay fair enough fair enough but that seems a reasonable first
76:54
- Tom: chance so um in a single shot meeting B what then um D is asking questions like
77:00
- Tom: uh was there anything discussed that wasn't answered um was there any you know
77:06
- Tom: fallacies uh any ambiguities were we using the right the um definitions uh in
77:12
- Tom: the right way um so you can get quite a lot of nuance uh once you've got the um
77:18
- Tom: transcript you can interrogate that transcript like um a live meeting right
77:25
- Tom: uh so what you're asking for there is um the ability to run a
77:31
- Tom: test go through all the different variations that happen and then jump into to a
77:36
- Tom: thread and Carry On Right talking right see even even in
77:42
- Tom: this setup with the uh the test you've got I mean I don't know how how quick you could do this but if you can run if
77:47
- Tom: you can add another test in the very next thing saying uh well let's go with that um was there anything discussed uh
77:55
- Tom: or um asked that wasn't fully answered let's see because it's script
78:01
- Tom: and it's uh is giving you here's the main point but then it's like let's drill down so what do you want to do buddy tell me uh so uh having brought in that uh transcript yeah um and uh it's
78:12
- Tom: produced the uh initial summary which we just looked at yeah the next thing would be to give it a prompt
78:19
- Tom: uh that would be um yeah uh give me um a list of uh all
78:27
- Tom: the questions that weren't fully answered any ambiguities and any definitions which
78:34
- Tom: appear to talk about the same thing but used
78:40
- Tom: different words to describe them let see I forgot the rest sorry uh give me a
78:46
- Tom: list of any questions that were asked but not answered any ambiguities any logical fallacies
78:55
- Tom: and any time where a similar topic was talked about but which
79:02
- Tom: a different definition appeared to be used so basically where did we get
79:07
- Tom: wrong you know there's all sorts of ways into yeah yeah okay so uh I don't have
79:14
- Tom: the testing framework in place to actually do the continuation of the next
79:20
- Tom: test case yet cuz I've only been running a single test case in these scenarios so that's why I have to pack it into the um
79:27
- Tom: original prompt as one one prompt here so that's that's the reason for the
79:33
- Tom: shortcoming uh I fix it soon but this is pretty cool right like I mean it's really [ __ ] cool it's
79:40
- Tom: like testing cuz uh uh when I find um when I going into meeting B I use it a
79:46
- Tom: lot right I'm asking the same questions right and so what I the point of this was that if I can get this test
79:53
- Tom: going oh what the fluff
79:59
- Tom: what what you seeing um
80:06
- Tom: error T testd it's not changed
80:13
- Tom: it called the function
80:19
- Tom: wrong I don't know probably called the function right but for some reason it didn't work sorry it called
80:25
- Tom: functions different hey um so what's the
80:31
- Tom: path must end with get TPS and the test case
80:36
- Tom: Runner test case Runner
80:42
- Tom: so I'll just add an extra error in
80:47
- Tom: here it seems to be doing the right thing but
80:55
- Tom: uh that could be something I haven't seen before but I've been
81:02
- Tom: dreading is that the B
81:07
- Tom: um with a slight change to a prompt it starts calling the functions
81:11
- Tom: differently with different parameters uh um need to lock that down
81:20
- Tom: why is it doing that I shouldn't um so it's either I've coded
81:26
- Tom: something wrong but I didn't do I didn't change anything from the last successful run I just added to the prompt yeah well
81:34
- Tom: that that's B free um because it do so it tried to call to
81:40
- Tom: call it tried to call the meetings agent not the meetings test
81:51
- Tom: file so that's the issue there okay and
81:58
- Tom: so that I'll take you to the prompt that's doing that this is um we're into pistol
82:05
- Tom: whipping torturing you yeah having said be nice to your Bots you got to
82:11
- Tom: Pistol this is this is extremely helpful for me by the way because it um
82:19
- Tom: was quite fun well uh I could do this all you can see where I struggle and you
82:25
- Tom: see what the process is yeah so I need to go into fixtures and I think I need
82:32
- Tom: to wipe this out uh test fire Runner test no no no
82:38
- Tom: ignore that so this is the
82:44
- Tom: agent that's running okay yep
82:50
- Tom: and it is looking for test. MD and it needs to it got told what to
82:56
- Tom: run because uh let me show you what it got told to [Music]
83:01
- Tom: do okay so this file that I just showed you got told called with
83:08
- Tom: this single argument this this is the text that went into it all right and
83:15
- Tom: wrong with there it's been prompted to you will be given a file name read
83:21
- Tom: this and then run the test within it but it read it read something completely
83:27
- Tom: different like it read so there there's two possible paths here uh well there's probably more but um uh so
83:37
- Tom: inside of meetings test. MD yeah have you told um the previous bot what a test
83:42
- Tom: is here's an example of what the test format is yes example absolutely okay so it knows what a test format is and when you say read this test and I read the
83:50
- Tom: file it's like that's a test happy okay and it got this it got this
83:55
- Tom: bit correct yeah agent
83:58
- Tom: okay path uh and [Music]
84:04
- Tom: then add case it got that correct
84:09
- Tom: too and
84:14
- Tom: then um and
84:19
- Tom: then it said this place was where it made a
84:24
- Tom: mistake test case [Music] Runner
84:30
- Tom: test case Runner test path must end with
84:35
- Tom: test. MD so and it called path with the
84:40
- Tom: agent not the test file so let me go and check my definition in the function yeah
84:49
- Tom: um who called that test file Runner right test case
84:52
- Tom: [Music] Runner [ __ ] [ __ ] that oh man I
84:58
- Tom: love this [ __ ] I really don't do love this [ __ ] path the path to the test file
85:06
- Tom: being
85:13
- Tom: run why are you constraining the uh the naming of the file why not just
85:20
- Tom: say uh use a test file and then it knows you could call it text yeah um read it it's a good idea to well for example if I didn't do that
85:28
- Tom: then this error wouldn't have occurred this this is actually wrong like it it
85:35
- Tom: tried to call the test Runner with the path to the agent file instead of the path to the test file well no the um
85:42
- Tom: that would still be an error but you're constraining it to um the file name yeah
85:49
- Tom: whereas it's uh you can call it you know j. text so long as it's actually a
85:56
- Tom: text sorry uh actually um a test what does it care you call it anything you
86:03
- Tom: want test. MD is uh something you know you just create it doesn't actually add
86:09
- Tom: anything semantically syntactically sure it's easier for us but why constrain it to that pattern
86:17
- Tom: why not um point it to an email that includes a
86:21
- Tom: test [Music] um you see what I'm saying um I'm
86:27
- Tom: probably not explaining it right but the more constraints that are unnecessary for the
86:33
- Tom: bot the more it's going to get weird um so what it's looking for is a
86:40
- Tom: test file now you've told it the format of a test file you can recognize a test F because of this
86:45
- Tom: format if I were to uh take a a written
86:51
- Tom: um piece of paper that was properly formatted as a test sent it yeah uh an
86:57
- Tom: image you should still run that test doesn't really care what T
87:02
- Tom: um yeah but my angle for doing that was that I
87:09
- Tom: want to be able to have multiple test files all across the file system and be
87:15
- Tom: able to identify them very rapidly without anything sophisticated so you know like if I'm
87:21
- Tom: not going to read every single file in the file system because that's too big but if I introduce a convention that
87:28
- Tom: it's just everything ining in. test. MD then I can do a very quick sweep and then fire them all up that was why
87:35
- Tom: I was doing that enough uh but that's a kind of indexing uh so
87:41
- Tom: piece um which maybe you want to read every file maybe you just want to read the file names and so on but when you
87:47
- Tom: feed it in all it needs to know is uh what's the format of the is this a
87:52
- Tom: test it doesn't need to know that you've named it right so um the um yeah
87:58
- Tom: but the agent that error of saying that the file name was incorrect that was on
88:04
- Tom: artifact side that was not on um bot side oh see I see yeah yeah
88:09
- Tom: okay here we go whoa whoa whoa whoa slow down buddy slow
88:14
- Tom: down um ah well I ran out of my buffer now so we could uh strip out
88:21
- Tom: duration anything you want to strip duration yeah
88:25
- Tom: I can do that it by roughly so we had start
88:33
- Tom: um oh we talked about duration du so I keep start and D
88:39
- Tom: are and text yeah
88:43
- Tom: it's it's not going to say much no it's not um
88:51
- Tom: we try anyway see but uh that's a hard limit which is uh because sometimes we
88:56
- Tom: do bang on for many hours um okay I'm going
89:02
- Tom: to how would
89:06
- Tom: we we would need to chunk it in this case right yeah but
89:12
- Tom: who wants to chunk who wants to chunk indeed buddy yeah cuz we could chunk it and then next week they go oh it's a
89:18
- Tom: million tokens I could just SW it was more anyway
89:25
- Tom: um well for this example probably just choose a shorter
89:30
- Tom: video doesn't matter who the video is just choose one random like 10 minute video as a URL
89:40
- Tom: it does seem like it's eating too much though
89:48
- Tom: yeah it's good for you to see the pain I have to go through like it's real fiddly
89:53
- Tom: to make this whole thing work together is good for me to actually feel your pain like is Lally more pain than my
89:59
- Tom: side like thanks for that man uh i' much rather think that you know you have no pain and therefore I feel good about myself oh and you now you're like
90:05
- Tom: actually yeah that whole empathy thing that that generates a lot of
90:12
- Tom: tokens so the size in bites was 178 ,000
90:18
- Tom: bytes which means that it should not have busted the tokens like it was not
90:25
- Tom: even close no um is this run still busting the
90:30
- Tom: Tok this run hasn't made it there yet there might be some errors in the
90:35
- Tom: API oh yeah yeah the API is uh well not completely to be trusted um
90:42
- Tom: it's FL as hell man yeah but you know Innovation all that kind of thing yeah
90:50
- Tom: yeah major outage 35 minutes oh dear impacting
90:56
- Tom: Lin for5 minutes it's nice to know that the chat
91:03
- Tom: gbt and the API seem to be like it sounds like chat GPT is using the API
91:09
- Tom: yeah you know so there's some extra stuff
91:14
- Tom: but more or less they're the same you know you got to uh take a hat
91:20
- Tom: off to you know any company that puts up their outages in a bar chart like that
91:26
- Tom: oh everyone does these days like we're going to do that oh yeah yeah but uh
91:32
- Tom: does everyone do that now I didn't do that well no one did back in the
91:38
- Tom: day instant report
91:42
- Tom: okay so it worked it worked
91:48
- Tom: but I think something else was going on like I do believe that that was a um API
91:55
- Tom: eror because the size of the file you know just isn't
92:01
- Tom: enough um and then what were we going to do meetings
92:06
- Tom: we don't have duration
92:09
- Tom: anymore yeah that that
92:14
- Tom: is that's data that we can actually infer between time stamps I'm not sure why they put in duration strange that
92:20
- Tom: they choose to put that in uh because the next time stamp start may be sign
92:27
- Tom: significantly later than the [Music]
92:33
- Tom: end of the previous time St plus duration cuz if you say something and then go quiet for 2 minutes without
92:40
- Tom: duration you don't know that that was 5 minutes of text you don't know where to clip your video if you want to snip the
92:46
- Tom: end I suppose I suppose um I choose a different way of doing
92:52
- Tom: that but yeah yeah yeah I
92:59
- Tom: suppose okay here we go it's going to work this
93:05
- Tom: time it's going to work it's going to work is it quick go go and sacrifice
93:13
- Tom: it I got a mouse
93:16
- Tom: well I've got a printer to sacrifice later on today which I'm going to
93:23
- Tom: enjoy a you know what you know what I think it's [Music]
93:30
- Tom: um I know what that I know why the tokens were big because I didn't Minify the
93:36
- Tom: Json I was pretty printing it with like a new line and a tab and all that
93:42
- Tom: you know it wasn't just that's going to be that's going to double the size well actually slightly
93:48
- Tom: more yeah why is this taking so
93:52
- Tom: long it shouldn't be so
93:58
- Tom: slow it's generating a lot of stuff it could be that uh it's just
94:04
- Tom: a bit [ __ ] right now it could be that we're an infinite Loop and you're about to be charge
94:09
- Tom: $127 I was so glad when that was your pro your your mistake not mine CU I was going [ __ ] what I
94:16
- Tom: done I was I was convinced it was it was me cuz I was kicking off Unk know
94:21
- Tom: perimeter parallel toal that's an error on their side man all right okay that's
94:28
- Tom: absolutely a legit parameter that we have been calling for the past [ __ ]
94:34
- Tom: all these tests that you saw around here that's their problem time is uh where's [ __ ]
94:42
- Tom: that now I'm getting call from the United States why I'm getting call um so uh yeah so get both answers
94:48
- Tom: back and then it'll make its best judgment if you say right okay so uh you
94:55
- Tom: know tell me what rot pie is uh it'll make a fres yeah you go then
94:59
- Tom: you can also say h give me two more Precision it's like ah I've got another
95:05
- Tom: answer yeah yeah that that makes sense that
95:11
- Tom: that feels good okays good so I'll Implement that into it's
95:16
- Tom: just yeah I I think we're getting closer and closer to a stable
95:23
- Tom: model these are all just little nuances that only really appear once you get into the weeds of it and the
95:30
- Tom: testing framework is key to being able to exercise these kinds of systems and make sure they behave how we want very
95:37
- Tom: much so very much so and um yeah the
95:43
- Tom: uh feels like um back chat is probably got still a rule um but as
95:51
- Tom: almost like a running task that the uh M can call on if you're asking for
95:59
- Tom: just Brute Force do stuff what would that be um like uh okay
96:05
- Tom: um I've just calculated or you know my agent just calculated two pies I'd like
96:11
- Tom: to save those into two different files please that wouldn't really be back chat
96:17
- Tom: though would it that would be um the files agent I would
96:23
- Tom: imagine yeah but backat is a combination of all the power operations that
96:29
- Tom: interact with Git well all of the agents many of the agents have the
96:36
- Tom: ability to interact with Git like the meeting bot was able to read from git
96:42
- Tom: and do some stuff I just I think what you're really meaning is you want like a system or
96:48
- Tom: file system level thing and you've attached that meaning to back chat but
96:54
- Tom: yeah I think it feels like it feels like just another bot really it's just
97:01
- Tom: yeah I think bechat dies now it's it's it's a cool concept it's a cool name but I think that it's yeah I know I know and I named so
97:08
- Tom: many things in the code repo back chat so that's annoying but
97:14
- Tom: um so m m takes over the Summoner and does the switching
97:19
- Tom: between threads yeah and switchboard creates new threads
97:27
- Tom: and makes them um makes M aware of those threads well
97:32
- Tom: switchboard there's always a base thread and if M can't handle it then it goes to
97:38
- Tom: the base thread which is what back chat used to be That's That Base thread is backchat I think so I think so
97:44
- Tom: this well let me stick into meeting part and yeah think about it sounds it sounds like it's unne it sounds like backchat is dead
97:53
- Tom: yeah yeah right uh just the time I need to go man all right to probably definitely need if you don't want to call it back chat then I do need a name
98:01
- Tom: for what this base thread is because base thread is
98:07
- Tom: unspecific can we call it well why not
98:14
- Scott: uh I know in the architecture how is just another thread yeah but we're
98:21
- Scott: talking about another agent it's like the um you know the first amongst
98:26
- Scott: equals um there seems to be a uh if it's you want to call it hell is that what
98:32
- Scott: you're going to say yeah yeah B if you go um you know up up up up up up up up
98:40
- Scott: up you can go up again you talking to you're talking to hell I think they should be hell yeah you are talking to
98:48
- Scott: hell but you want to name the whole thread as hell the whole black thread as
98:53
- Scott: hell I do H's thread okay all right that's cool and uh I don't know I'll
98:59
- Scott: just I I need to defer that rename for a bit cuz that's going to take a lot of time so I need to leave it named as back
99:06
- Scott: chat for now and then I'll rename it to how later don't worry about renaming and send it um also I'm um there might be a
99:14
- Scott: better way of talking about it because my we threw out as bit of
99:20
- Scott: a name yeah true and it might not be the best but uh there is a name for that if
99:27
- Scott: you go all the way up yep out of every Rabbit Hole you can you can't go any
99:34
- Scott: further yep that thing that's what we're talking about yep
99:40
- Tom: yeah right okay all right um cool I'll copy and
99:47
- Tom: paste this uh meetings output over to you so you can have that for shits and giggles and then um nice yeah uh I am
99:55
- Tom: I've got limited ability this afternoon being start the afternoon and
100:00
- Tom: mentions but um on my side uh made quite
100:07
- Tom: good progress I think especially with this uh this intest to be brilliant but
100:14
- Tom: bringing in everything we've been talking about the last 6 months yep aw in order to to generate uh adjust Time
100:22
- Tom: website awesome um and by that I mean you know here's uh 20 chunks of
100:30
- Tom: text uh that depending on what you're interested in displays what you're interested in which seems reible that's
100:38
- Tom: pretty damn good man yeah um and also uh as a throw side I've
100:45
- Tom: already got a bot I'm not sure you at the moment but just take my word on this um taking each one of these things and
100:52
- Tom: cre a blog post right um uh well I was I was thinking more of
100:59
- Tom: um uh I don't know what the right word is it's like uh today we talked about this a daily report summary um yeah it's
101:06
- Tom: like yeah a log of what were we talking about anyway that's that's true sorry
101:12
- Tom: that cool anyway got to go okay buddy uh that was deeply uh deeply enjoy
101:19
- Tom: sweet I enjoyed that oh well plenty more to come I think
101:25
- Tom: yeah okay I'll see you later talk to you later okay see you bye

