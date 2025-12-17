%%[This page was last updated on ==2025-11-09 @00:59==]%%


<panel type="info"  collapsed>
<div slot="header">

### 1. SRIV..SHIT `@HarshitSrivastavaHS` (**51** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/20#discussion_r2405184687" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Revert parsing logic. The loop introduces an unnecessary O(N) performance here compared to the original O(1) HashMap lookup.
Could you please clarify what the issue was with the former approach?

Another question, could you clarify why to move away from the split(" ", 2) approach?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/20#discussion_r2405202368" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I realised why you changed it. Shouldn't we make each command a single continuous token (like "addpet", instead of "add pet")?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/20#discussion_r2405214716" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I guess single token commands would be better :))
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/23#discussion_r2407139351" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

we already have a PetList object named pets on line 31
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/23#discussion_r2407146261" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

can just do ArryaList&lt;Treatment> treatments
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/23#discussion_r2407180104" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This will not work if any of the parts have a whitespace, for example
"p/10 s/name here ig d/2025-10-15 t/ sometype"
on splitting with whitespace as the delimiter:
-> ["/p10", "s/name", "here", "ig", "d/2025-10-15", "t/", "sometype"]
petIndex = 10, name = "name", date = "2025-10-15", type = out of bound ? 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/25#discussion_r2410167943" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The indentation is incorrect here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/25#discussion_r2410204321" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This splits the args at every one+ whitespace. 
This would split such a string incorrectly:
- "n/ pet name i/index of the treatment"
- - ["n/", "pet", "name", "i/index", "of", "the","treatment"];
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/25#discussion_r2410207420" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same as above
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/26#discussion_r2411101138" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Incorrect indentation i think?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/26#discussion_r2411142531" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nvm, it's correct
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/43#discussion_r2432034286" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

can just do: pet.addTreatment(newTreatment);
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/43#discussion_r2432035667" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

no need to import ArrayList
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/71#discussion_r2438920192" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Missed turning off the logger (LOGGER.setLevel(Level.OFF)) :melting_face: 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/71#discussion_r2440055605" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

hihi, sorry, since we're logging to a file now, we do not need this
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/74#discussion_r2441641369" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe  mute the logs during the test, just add:
'''java
    @BeforeAll
    static void muteLogs() ``{``
        LogManager.getLogManager().reset();
        Logger root = Logger.getLogger("");
        root.setLevel(Level.OFF);
    ``}``
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/79#discussion_r2446851907" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I feel like it'd be better to just add a getter in the treatment class.
This kinda increases the coupling between treatment and this class and might break if anybody updates the toString method :smiling_face_with_tear: 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/79#discussion_r2446855448" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I feel this should be in PetList too :smiling_face_with_tear: 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/77#discussion_r2447123709" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This is already imported at line 16 (FindCommand)


</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/81#discussion_r2448930087" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The inheritance here seems incorrect to me 🥲 
It should follow "is a" relationship, so: SummaryCommand is a FilterTreatmentByDateCommand, which it isn't 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/89#discussion_r2452102386" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Since "Command" is an interface, it should be ..|>
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/89#discussion_r2452451833" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

pets here is defined as an attribute, however, there's also an association arrow bw this class and the petList. I think this would be incorrect.

Same for the other diagram
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/94#discussion_r2452602938" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This should be public
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/94#discussion_r2452637332" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should be o--
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/94#discussion_r2452672654" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

According to the notes, it should be the other way around I think :smiling_face_with_tear: 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/89#discussion_r2452692690" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LOGGER is a static variable ``{``static``}``
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/89#discussion_r2452694280" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps can show the aggregation/composition here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/89#discussion_r2452694932" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same as above, should be static
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/89#discussion_r2452695582" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2462684771" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LOGGER is a static variable, just add ``{``static``}`` before it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2462685624" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same as above
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2462689548" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Since Command is an interface, it should be dotted lines
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2462689600" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

It should be '''&lt;&lt;Interface>>'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2462689810" expanded>
<div slot="header">

**34 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same as the other comment
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2462708990" expanded>
<div slot="header">

**35 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This comment is for both the sequence diagrams:
1. Self invocation creates another activation bar which is missing in the diagram.
1. You do not need to show User, CuddleCare, Parser, CommandsWithArgs and stuff. Unless I'm mistaken, the scope of the diagram should be this class only, you don't have to tell how this class was called and who it returns the value to
1. About the first point, I guess "parse dates" and stuff aren't really different methods, if so, the entire arrow is wrong, it shouldn't be there

For the second point, it should just start with an arrow called the exec method, and should end with exec returning a value
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2462871419" expanded>
<div slot="header">

**36 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can change these to this instead:
'''&lt;-- FTC : "&lt;MSG">'''

Like, currently the "return" arrow seems to be going to the right instead of the left.
This should fix it.

There's one more in this file on line 23
and then there are some in the FindTreatmentCommandSequence as well
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2466299542" expanded>
<div slot="header">

**37 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

ooo, yup. Looks good except this&hat;&hat;
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/124#discussion_r2477551085" expanded>
<div slot="header">

**38 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

perhaps could've made a single method with arguments, something like:
`printUsage(String syntax, String example)`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/134#discussion_r2478323018" expanded>
<div slot="header">

**39 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The cross is incorrect here, can replace it with -->
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/134#discussion_r2478375255" expanded>
<div slot="header">

**40 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think this is used for calling a new method, can just write this on the next arrow (command failed one)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/124#discussion_r2478384350" expanded>
<div slot="header">

**41 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

true, but without it i think it might've been better in the class itself, and these methods can't really be reused by other classes anyway (since they're too specific)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/150#discussion_r2478418053" expanded>
<div slot="header">

**42 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The url is incorrect
the correct url would be: team/gohjieling834.html
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/224#discussion_r2484560444" expanded>
<div slot="header">

**43 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

perhaps can keep the greet() method and replace the println method with print greet message?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/229#discussion_r2485475676" expanded>
<div slot="header">

**44 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The print method in Ui class is a static method, and hence the notation should be `&lt;&lt;class>>\nUi` instead of `:Ui`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/229#discussion_r2485477262" expanded>
<div slot="header">

**45 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The exec method in `:EditPetCommand` is calling the print method in Ui, and yet `exec` seems to be ending before the method in Ui ends
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/229#discussion_r2485478546" expanded>
<div slot="header">

**46 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

In the alt block, the if statement returns `Pet not found` and the else block returns `success`
if the method returns there, the rest of it (calling `print` in Ui) would never occur
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/229#discussion_r2485479836" expanded>
<div slot="header">

**47 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same issues here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/229#discussion_r2485669006" expanded>
<div slot="header">

**48 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The Ui class has 2 returns, one to the user and one to the EditPet class
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/249#discussion_r2488467473" expanded>
<div slot="header">

**49 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

in the alt block (if), it should still return back to the `:CuddleCare`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/249#discussion_r2488472718" expanded>
<div slot="header">

**50 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

perhaps keep this line but at line 30 (just remove the print message)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/249#discussion_r2488480034" expanded>
<div slot="header">

**51 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

yup, `"&lt;&lt;class>>\nUi"`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432495954" expanded>
<div slot="header">

**52 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

oh oki, will capitalize it. thanks :saluting_face: 

yes, so, logger.setLevel sets the minimum log level at which the logger will record messages
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432498114" expanded>
<div slot="header">

**53 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

wait is it? but they taught us lambda too :cry: 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432540123" expanded>
<div slot="header">

**54 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

alright, i'll change it then :sob: 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/67#discussion_r2438843943" expanded>
<div slot="header">

**55 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

It's the same, but i've updated it :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/67#discussion_r2438863957" expanded>
<div slot="header">

**56 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

It's enabled by default so i removed it :eyes: 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/100#discussion_r2468299551" expanded>
<div slot="header">

**57 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

- [x] Moved it to a different method
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/100#discussion_r2468303297" expanded>
<div slot="header">

**58 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

I kinda used a guard case here to make the "happy path" more prominent _even though both are a happy path here, lolll_
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/117#discussion_r2472521442" expanded>
<div slot="header">

**59 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

thanks, done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/116#discussion_r2473127292" expanded>
<div slot="header">

**60 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Nope, my bad. It's supposed to be a single space only :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/117#discussion_r2478249279" expanded>
<div slot="header">

**61 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

it does since it's an alt frame, the prev notation was incorrect
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/issues/19#issuecomment-3369988228" expanded>
<div slot="header">

**62 :octicon-comment:** %%(other comment)%%
</div>

Implemented in PR #18 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/22#issuecomment-3374907346" expanded>
<div slot="header">

**63 :octicon-comment:** %%(other comment)%%
</div>

closes #21 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/23#issuecomment-3374909180" expanded>
<div slot="header">

**64 :octicon-comment:** %%(other comment)%%
</div>

closes #1 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/20#issuecomment-3374912313" expanded>
<div slot="header">

**65 :octicon-comment:** %%(other comment)%%
</div>

closes #9 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/31#issuecomment-3382269327" expanded>
<div slot="header">

**66 :octicon-comment:** %%(other comment)%%
</div>

Closes #7 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/122#issuecomment-3460911231" expanded>
<div slot="header">

**67 :octicon-comment:** %%(other comment)%%
</div>

About the format in which it's saved, how're you going to figure out if you're loading the file correctly (since it's being saved as plain readable text)?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/issues/189#issuecomment-3475819754" expanded>
<div slot="header">

**68 :octicon-comment:** %%(other comment)%%
</div>

<img width="908" height="549" alt="Image" src="https://github.com/user-attachments/assets/e05bd581-02c9-4459-8d62-e84d8b7b5b66" />
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/issues/190#issuecomment-3475822423" expanded>
<div slot="header">

**69 :octicon-comment:** %%(other comment)%%
</div>

The Logger creates a file and logs to it, the output is not to the console.
<img width="863" height="579" alt="Image" src="https://github.com/user-attachments/assets/b264b3a7-14af-438e-851b-dbaceb7e0fbe" />
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/issues/167#issuecomment-3477569469" expanded>
<div slot="header">

**70 :octicon-comment:** %%(other comment)%%
</div>

Issue with Add-pet #178 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/issues/166#issuecomment-3479224841" expanded>
<div slot="header">

**71 :octicon-comment:** %%(other comment)%%
</div>

Fixed in #222 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 2. GAO ..NETH `@duckyfuz` (**48** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/47#discussion_r2423386795" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I really like this! Very succinct and clear
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/47#discussion_r2423386952" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you have given examples of how the program can will behave.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/47#discussion_r2423387126" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think the FAQ format is suitable for answering frequently asked questions. Good job!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/47#discussion_r2423387380" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Initializing this as static is suitable. Great approach.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/47#discussion_r2423387822" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good documentation
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/47#discussion_r2423387979" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job wrapping in a try catch. To prevent runtime errors from breaking the program.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/47#discussion_r2423388061" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice to see that you've been careful to not commit files that should not be committed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/53#discussion_r2425167173" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

useful documentation that tells me it's chronological!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/53#discussion_r2425167474" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

great logging here to ensure that expense was created
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/53#discussion_r2425167785" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

i think this is good use of throwing errors - we cannot let the expense be null. very protective.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/53#discussion_r2425168180" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

great use of BeforeEach and AfterEach decorators to reduce boilerplate code!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/53#discussion_r2425168397" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good edge case!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/60#discussion_r2441882318" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

mmmm nice abstraction here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/60#discussion_r2441882686" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice that the code is so safe
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/60#discussion_r2441883303" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

indeed this is a better name
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/60#discussion_r2441883571" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

i enjoy the abstraction here via an enum
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/60#discussion_r2441883967" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thanks for updating the tests too!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/70#discussion_r2445459546" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

private static is good for this type of strings!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/70#discussion_r2445460799" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

amazing refactoring job here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/70#discussion_r2445464256" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

agree that keeping Ui.printError inside each case is better since it keeps the command's guard and message together, so we see the rule where the command runs
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/70#discussion_r2445464847" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

beautifully crafted code here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/142#discussion_r2465910620" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You've identified diverse user roles, from students to organizers and directors, highlighting a well-rounded approach to understanding user demographics.
There is a recognition of varying financial needs, such as managing stipends, tracking expenditures, and handling shared funds, acknowledging the complexity of financial management tasks faced by different users.

Good job Jordan!!!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/142#discussion_r2465910701" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how everything is neatly structured into a clean and concise table!


</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/142#discussion_r2465914598" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how the required functionalities are neatly categorized, focusing on core financial tasks like recording expenses, logging incomes, setting budgets, and exporting data.

Effort was also taken to mark complexity levels (indicated by asterisks: * to ***) suggest a prioritization or difficulty level, helping us identify which features to address first.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468957822" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM! This is an excellent clarification.

The original documentation was misleading by stating all parameters could be in any order. This change correctly distinguishes between the compulsory parameters (which remain flexible) and the optional des/ parameter, which has a specific constraint.

Adding the rule that des/ must be placed last—and explaining why ("everything after des/ is treated as part of the description")—is a crucial improvement. This makes the documentation more accurate and will prevent user confusion and parsing errors.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468959167" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468968051" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

That's a robust and modular utility method, findFirstPrefixIndex, that is essential for reliable command parsing. Good job.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468971791" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch here! It's great that you've made logging and throwing error for safety a habit.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468975733" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great! This is indeed a better way to handle the case where split = -1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468977590" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great that you've spotted this edge case
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468980982" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good happy path chosen here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/147#discussion_r2468984498" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good test here for throwing then a non finite amount is input
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/235#discussion_r2483774308" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great work identifying where the issue was! Required amazing deduction skills
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/239#discussion_r2483776781" expanded>
<div slot="header">

**34 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think it's good that this logic is encapsulated in a function
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/239#discussion_r2483776851" expanded>
<div slot="header">

**35 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

yes, more than 0 is a better error to show here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484817590" expanded>
<div slot="header">

**36 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good catch here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484817686" expanded>
<div slot="header">

**37 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

another great formatting catch, thanks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484817802" expanded>
<div slot="header">

**38 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

great! seems very logical to move this to a method of its own
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484818061" expanded>
<div slot="header">

**39 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good catch here - indeed we should check for the existance of each prefix
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484818153" expanded>
<div slot="header">

**40 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

great example of good debugging logs
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484818529" expanded>
<div slot="header">

**41 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I agree that having boolean flags for the existance of each property is a good idea as it makes the code much more readable
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484818613" expanded>
<div slot="header">

**42 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good formatting done here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484818728" expanded>
<div slot="header">

**43 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Indeed this is a great edge case to check for
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/273#discussion_r2484818946" expanded>
<div slot="header">

**44 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great that you've remembered to update the text ui tests!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/291#discussion_r2486809437" expanded>
<div slot="header">

**45 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good catch here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/295#discussion_r2487343601" expanded>
<div slot="header">

**46 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for your hard work
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/295#discussion_r2487344753" expanded>
<div slot="header">

**47 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch here!

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/295#discussion_r2487345329" expanded>
<div slot="header">

**48 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Yes, this is a good case - where the user is technical
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/2#issuecomment-3354695605" expanded>
<div slot="header">

**49 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/3#issuecomment-3354695894" expanded>
<div slot="header">

**50 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/5#issuecomment-3354730446" expanded>
<div slot="header">

**51 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/87#issuecomment-3437008311" expanded>
<div slot="header">

**52 :octicon-comment:** %%(other comment)%%
</div>


Fixes: https://github.com/AY2526S1-CS2113-W12-4/tp/issues/86
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/87#issuecomment-3437008638" expanded>
<div slot="header">

**53 :octicon-comment:** %%(other comment)%%
</div>

Fixes: https://github.com/AY2526S1-CS2113-W12-4/tp/issues/67

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/90#issuecomment-3437124069" expanded>
<div slot="header">

**54 :octicon-comment:** %%(other comment)%%
</div>

Fixes: https://github.com/AY2526S1-CS2113-W12-4/tp/issues/89
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/90#issuecomment-3450759302" expanded>
<div slot="header">

**55 :octicon-comment:** %%(other comment)%%
</div>

Fixes: https://github.com/AY2526S1-CS2113-W12-4/tp/issues/89
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/220#issuecomment-3476428246" expanded>
<div slot="header">

**56 :octicon-comment:** %%(other comment)%%
</div>

can you take a screenshot of your root dir
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/177#issuecomment-3476452751" expanded>
<div slot="header">

**57 :octicon-comment:** %%(other comment)%%
</div>

fixed by: https://github.com/AY2526S1-CS2113-W12-4/tp/pull/233
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/189#issuecomment-3476453627" expanded>
<div slot="header">

**58 :octicon-comment:** %%(other comment)%%
</div>

actually removed bc someone said the diagram was too long. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/238#issuecomment-3476467532" expanded>
<div slot="header">

**59 :octicon-comment:** %%(other comment)%%
</div>

Fixes: https://github.com/AY2526S1-CS2113-W12-4/tp/issues/225

</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 3. LUKE.. TAN `@lukeai-tan` (**48** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/3#discussion_r2377741748" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/38#discussion_r2417563117" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

For this, you could consider putting this into UpdateCommand itself for Separation of Concerns, where an UpdateCommand constructor takes in the argument from the args variable, translate it into an update command.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/38#discussion_r2417564773" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice job on the JUnit tests.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/38#discussion_r2417569817" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

For SoC, the parser class generally shouldn't be controlling what happens to the InternshipList. You could consider making the UpdateCommand responsible for that instead.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/38#discussion_r2418467934" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

True. Maybe that can be done once the InternshipList's arraylist is made static.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/50#discussion_r2426226441" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nicely done UI
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/50#discussion_r2426228006" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of constants to prevent magic strings.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/51#discussion_r2426267934" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
        ``}`` catch (Exception e) ``{``
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/51#discussion_r2426329909" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job on the throrough invalid command checks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/52#discussion_r2426340294" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job on the JUnit tests!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/42#discussion_r2426572813" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great job on the JUnit tests. Very thorough!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/59#discussion_r2435359509" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good attempt at assertion, but in this case, the assertion you wrote will pass regardless of whether listAll() fails or not. You typically want to check for a condition that must hold in this specific line.

Also, I think an assertion is not necessary here, since you've already covered the assertions in the listAll() logic in InternshipList. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/59#discussion_r2435367833" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good assertion after isEmpty edge case
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/59#discussion_r2435414749" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Unfortunately, `assert true` doesn't provide any signal for whether execute is called or not. I believe assertion messages are only printed if the assert condition is false. 
So given two cases:
Case 1: ListCommand fails, execute() is never called, no message gets printed.
Case 2: ListCommand succeeds, no message gets printed.

You could consider using logging instead, like so:

'''suggestion
       logger.info("Executing list command...");
       InternshipList.listAll();
       logger.info("List command executed successfully.");
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/62#discussion_r2438563549" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider avoiding magic numbers for the indexes:

Such as:
```
final int IDX_COMPANY = 0;
final int IDX_ROLE = 1;
final int IDX_DEADLINE = 2;
final int IDX_PAY = 3;
final int IDX_STATUS = 4;
```

Just realised we haven't been doing that for the parsing methods too.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/62#discussion_r2438564497" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Avoid magic numbers for these too.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/62#discussion_r2438570617" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Excellent use of assertions to catch programming errors early
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/62#discussion_r2438572890" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

It’s good that you log and print user-visible warnings. This helps provides visibility for both the developer and the user.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/65#discussion_r2442420329" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Need a check that the pay integer is at least 0 too
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/65#discussion_r2442421992" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good choice of using Set for fast contains() lookup. Using Set.of() also ensures immutability, which is good.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/78#discussion_r2445394985" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Avoid using magic numbers for the parameter for the constructor's parameters.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/78#discussion_r2445403017" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

super() can be omitted since the superclass Command does not have any constructor.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/78#discussion_r2445404023" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Avoid magic numbers here.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/78#discussion_r2445464099" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Interesting use of wildcard type bound for the Comparator, but I don't think it is necessary here since the Internship class is the base class, so there are no superclasses above it. This would work best for cases such as having multiple Internship subclasses.

'''suggestion
    public static Comparator&lt;Internship> SortByDeadline;
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/78#discussion_r2445469759" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Avoid magic numbers for the ListCommand constructor args.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2446855156" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You could consider breaking this method up into smaller methods because it is getting quite long.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2446953408" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could you also add an enum or checks for the valid statuses: Pending, Interested, Applied, Interviewing, Offer, Accepted, Rejected.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2446963314" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good JUnit tests.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2446981507" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I know this isn't your line of code but could you help amend this, thanks!

'''suggestion
    public static final int INDEX_MAXLEN = 5;
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2446997135" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

For the UpdateCommand specific conditions, you could consider making a more generic exception for all of them, up to you. For the reused ones like `Invalid update command format. Use: update INDEX field/VALUE ...`, you could make a custom `InternityException` method in the `InternityException` class.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2447020747" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Boolean naming conventions

'''suggestion
        boolean isUpdated = false; 
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2447026193" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Sick tests.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/79#discussion_r2448546575" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

For this, I think it should be parseOneBasedIndex since the input is the user's side index, which is then converted to zero based index for the logic of the UpdateCommand.

'''suggestion
        int index = parseOneBasedIndex(idxAndTagged[0]);
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/103#discussion_r2469116387" expanded>
<div slot="header">

**34 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nicely done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/103#discussion_r2469119058" expanded>
<div slot="header">

**35 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Tests are very extensive. Well done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/104#discussion_r2469854339" expanded>
<div slot="header">

**36 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

For this diagram, you could make it more centered around the DeleteCommand instead, since the InternityManager to the ArgumentParser sequence was already described in the logic component.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/108#discussion_r2473065438" expanded>
<div slot="header">

**37 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good fix. Helps reduce redundancy in multiple if statements.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/108#discussion_r2473147753" expanded>
<div slot="header">

**38 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Excellent. Very extensive Java docs
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/106#discussion_r2474253926" expanded>
<div slot="header">

**39 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job splitting up for the more concise exception messages.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/112#discussion_r2474541194" expanded>
<div slot="header">

**40 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You could put this at the top or bottom of Step 4, for the reader's easy reference. You can also omit the "### Sequence Diagram###"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/112#discussion_r2474549926" expanded>
<div slot="header">

**41 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
#### Design Considerations
'''

Just for consistency with the other feature sections.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/112#discussion_r2474568747" expanded>
<div slot="header">

**42 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This can be omitted as well since the main focus of this section is about how update command carries out its task. The saving data is elaborated on in the Storage feature.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/112#discussion_r2474575593" expanded>
<div slot="header">

**43 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This can be omitted. This is part of the InternityManager and storage relationship.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/113#discussion_r2476473992" expanded>
<div slot="header">

**44 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job abstracting out the Ui related parts from Internshiplist into Ui.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/113#discussion_r2476475394" expanded>
<div slot="header">

**45 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good eye. Enums should be in pascal case.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/173#discussion_r2484776052" expanded>
<div slot="header">

**46 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
    public static void findInternship(String keyword) ``{``
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/173#discussion_r2484776215" expanded>
<div slot="header">

**47 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
        if (nearest == null) ``{``
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/173#discussion_r2484776701" expanded>
<div slot="header">

**48 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
                    thisInternship.getRole().toLowerCase().contains(keyword.toLowerCase())) ``{``
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/75#discussion_r2459097257" expanded>
<div slot="header">

**49 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Alright. Will add logging.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/75#discussion_r2459097792" expanded>
<div slot="header">

**50 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Will fix this. Thanks for pointing that out!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/75#discussion_r2459260165" expanded>
<div slot="header">

**51 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Good eye. Fixed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/109#discussion_r2474170197" expanded>
<div slot="header">

**52 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Updated!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/109#discussion_r2474181335" expanded>
<div slot="header">

**53 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Fixed this.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/109#discussion_r2474212584" expanded>
<div slot="header">

**54 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Done!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/3#issuecomment-3332161338" expanded>
<div slot="header">

**55 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/98#issuecomment-3452377567" expanded>
<div slot="header">

**56 :octicon-comment:** %%(other comment)%%
</div>

Restructured the packages:
logic now contains cli and commands packages
storage now contains Storage.java

Edited Developer Guide accordingly
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 4. THEN..ELLE `@noellethen` (**35** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/46#discussion_r2423370856" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you broke up the long line by using indentations here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/46#discussion_r2423371244" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how there is info-level logging for easier debugging in case anything goes wrong!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/46#discussion_r2423371605" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This method seems a bit long. Perhaps it can be shortened, or some parts of it can be abstracted?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/57#discussion_r2440255241" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of error handling here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/57#discussion_r2440258261" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like the comprehensive checks here for bad inputs!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/73#discussion_r2447710982" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Succinct information to describe the class! 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/73#discussion_r2447713159" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Diagram is very clear!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/81#discussion_r2454175666" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good effort in checking for bad inputs!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/81#discussion_r2454179636" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This seems to only abstract out one line of code (the println statement). Perhaps it may not be meaningful?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/81#discussion_r2454182540" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of logging for easier debugging!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/90#discussion_r2459035666" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good indentation for better readability!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/90#discussion_r2459037256" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like that you cut down the LOCs to prevent long methods!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/95#discussion_r2461547467" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you included the .puml files for easy reference!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/95#discussion_r2461549447" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good error handling here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/95#discussion_r2461551549" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like that you included assertions to keep the code as defensive as possible!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/95#discussion_r2461554151" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great checking for bad inputs here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/119#discussion_r2463913830" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for updating!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/125#discussion_r2463925702" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for adding more commands to the summary table!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/125#discussion_r2463925941" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for updating the method to be more accurate!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/125#discussion_r2463926184" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Appreciate the effort to update everything to "des" instead of "desc"!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/129#discussion_r2464482876" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for updating the UG comprehensively!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/161#discussion_r2474384360" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/163#discussion_r2474416740" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe the headers should be unnamed instances? E.g. :FinTrack instead of FinTrack
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/163#discussion_r2474425459" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I don't think Ui uses Parser? If I'm not wrong, every component is handled by FinTrack.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/163#discussion_r2474472051" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/163#discussion_r2474494434" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Yay looks good!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/174#discussion_r2483178013" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good error checking here!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/174#discussion_r2483178091" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like that you included unit tests for this feature as well!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/233#discussion_r2483755286" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

It's great to have this restriction to prevent potential errors!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/234#discussion_r2483763148" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Informative error message!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/234#discussion_r2483763331" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for adding test cases too!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/285#discussion_r2486559813" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for adding this!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/286#discussion_r2486572571" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great diagram!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/286#discussion_r2486573511" expanded>
<div slot="header">

**34 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for updating the test cases as well!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/296#discussion_r2487424682" expanded>
<div slot="header">

**35 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Looks good!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/1#issuecomment-3354695549" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/8#issuecomment-3354728762" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/240#issuecomment-3476493085" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/250#issuecomment-3476650841" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/255#issuecomment-3477523419" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/256#issuecomment-3477523666" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/257#issuecomment-3477523823" expanded>
<div slot="header">

**42 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/258#issuecomment-3477523921" expanded>
<div slot="header">

**43 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/259#issuecomment-3477525582" expanded>
<div slot="header">

**44 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/221#issuecomment-3477613161" expanded>
<div slot="header">

**45 :octicon-comment:** %%(other comment)%%
</div>

Closed under #261 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 5. LIM .. JIN `@yikjin` (**32** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/51#discussion_r2431214799" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Unnecessary because all entries are in the root '.gitignore' file already
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/51#discussion_r2431217009" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Not needed because we are using Java, not Kotlin (my IDEA doesn't generate this file for Java projects, does it for you?)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440684032" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Main method shouldn't throw any exceptions like that, ideally should handle in `try`-`catch` block, so that a useful error message can be shown instead of just crashing the app
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440685708" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Wrap in `try`-`catch` block, see comment above
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440736173" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This method shouldn't be in the `Course` class, since it is not representing a course. Rather, it's a method relating to parsing, so perhaps either lump it with the parser, or have a new course parser class?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440737284" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same thing for this, it's not representing a session, rather it's a session parser method
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440740930" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Concatenating strings this way doesn't cause them to be on separate lines. I did it that way originally because having one line of error message, then next line of usage hints is clearer for the user I feel. Of course, feel free to disagree here.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440741783" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same thing here, see comment above
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440742158" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This too
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440744338" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nit: add newline in between


'''suggestion
        String line;

        while ((line = buffer.readLine()) != null) ``{``
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440751453" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I don't think it's a good idea to have tests that potentially throws exceptions, make sure they don't throw one to begin with by using `assertDoesNotThrow()`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440752365" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same thing for this, see comment above
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440753641" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nit: remove extraneous newline

'''suggestion
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2440755877" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nit: add newline in between


'''suggestion
                    Course matchingCourse = null;

                    for (Course c : courses) ``{``
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442465344" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Erm 7 spaces?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442465826" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Extraneous space
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/105#discussion_r2467863445" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Is there any reason for doing this, instead of just using `logger.log()`?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/105#discussion_r2467874545" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Why do this and then have to deal with reflection tho? Why not just e.g. follow how [EditSessionCommandTest.java](https://github.com/AY2526S1-CS2113-W14-2/tp/blob/9e52016207638d9e93be7468765bdc6607ccfdcb/src/test/java/arpa/home/nustudy/command/EditSessionCommandTest.java#L33-L41) does it, with initialising `new CourseManager()`, `new SessionManager()`, and `new Course()` in the `@BeforeEach void setUp()` method?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/105#discussion_r2467888696" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I uh don't think we should do reflection in the code? Since 1) it's not taught to us and looks quite out of place here and 2) the code base isn't that complicated to need reflection?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/105#discussion_r2467890509" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

See [this comment below](https://github.com/AY2526S1-CS2113-W14-2/tp/pull/105/files#r2467874545) for more
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/109#discussion_r2471541524" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Unnecessary changes, since Markdown automatically increments the numbers in the generated output, so for simplicity we can just use `1.` for numbered lists
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/187#discussion_r2486934267" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe can be more specific, so it doesn't look like a duplicate?


'''suggestion
                 Add a study session with date      add &lt;course code> &lt;hours> &lt;date>    add CS2113 5 23/10/2025
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/194#discussion_r2487052639" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The `[date]` may be confusing, split into 2 sections instead?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/194#discussion_r2487101278" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

`date` not specified in this section, so is confusing (where it come from?)

Just say this command will create with today's date or something like that will do.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/194#discussion_r2487103821" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think use the whole parameter better


'''suggestion
> `&lt;study duration in hours>` should be 0.5 to 24
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/194#discussion_r2487104977" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same for this


'''suggestion
> `&lt;study duration in hours>` should be 0.5 to 24
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/194#discussion_r2487105776" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same for this


'''suggestion
> If `&lt;date>` is not provided, today's date will be used.
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/213#discussion_r2487502047" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I thought we decided to do away with the "double format" wording, since end users who are not technical don't know what that is?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/220#discussion_r2487508962" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Date is not a compulsory field, so maybe something like this would make more sense?


'''suggestion
1. System validates course existence, hours, and date if specified
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/213#discussion_r2487513927" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Extraneous space at the end.


'''suggestion
NUStudy supports hours starting from 0.5 to 24, with 0.5 increment only.
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/223#discussion_r2487555014" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Random capitalisation of "Course"

'''suggestion
     Reset a course                     reset &lt;course>                      reset CS2113
     Reset all courses                  reset all                           reset all
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/223#discussion_r2487555787" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Random capitalisation of "Course"


'''suggestion
                 Reset a course                     reset &lt;course>                      reset CS2113
                 Reset all courses                  reset all                           reset all
'''
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/107#discussion_r2471540441" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

See [the below comment](https://github.com/AY2526S1-CS2113-W14-2/tp/pull/107#issuecomment-3459212829)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/38#issuecomment-3398255248" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

Resolved in #39
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/43#issuecomment-3400790740" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

Fixed in #44
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/41#issuecomment-3400791967" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

Fixed in #42
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/107#issuecomment-3459212829" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

Yea, the numbering is correct, Markdown automatically increments the numbers in the generated output, so for simplicity we can just use `1.` for numbered lists
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/152#issuecomment-3480397269" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

Upgrading to severity high, because:

1. The log output is severely distracting and clutters up the console, to the point where it's hard to find where the actual output of the commands are
2. The output for the commands with logging now deviates from user guide
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/156#issuecomment-3480405084" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

Upgrading to severity high, because:

1. The log output is severely distracting and clutters up the console, to the point where it's hard to find where the actual output of the commands are
2. The output for the commands with logging now deviates from user guide
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/126#issuecomment-3481286793" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

Not planned, because users may want to use this functionality to see separate study sessions that are on the same day, instead of the sessions being lumped up into one.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/137#issuecomment-3481311055" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

Fixed in #173 by @t-kandasami.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/145#issuecomment-3481481273" expanded>
<div slot="header">

**42 :octicon-comment:** %%(other comment)%%
</div>

Fixed in #185.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/7#issuecomment-3481483672" expanded>
<div slot="header">

**43 :octicon-comment:** %%(other comment)%%
</div>

Closing in preparation for `v2.1` release.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/12#issuecomment-3481484713" expanded>
<div slot="header">

**44 :octicon-comment:** %%(other comment)%%
</div>

Closing in preparation for `v2.1` release.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/201#issuecomment-3482036745" expanded>
<div slot="header">

**45 :octicon-comment:** %%(other comment)%%
</div>

Fixed in #222.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 6. JORD..HENG `@JordanTwz` (**31** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/43#discussion_r2423350624" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The added Javadoc comments greatly improve the clarity and maintainability of the code.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/51#discussion_r2424025470" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of Java’s built-in logging to provide more visibility into potentially problematic instantiations of Expense.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/51#discussion_r2424027630" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The use of assertions is helpful during development. However, since assertions can be disabled at runtime, relying on them for validation may be risky.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/51#discussion_r2424029447" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Excellent addition of explicit checks and logging before throwing exceptions. This will help catch and diagnose issues earlier.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/51#discussion_r2424031180" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

As with Expense, this is a robust way to enforce valid object construction and provide clear diagnostics.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/51#discussion_r2424035980" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job updating the test to reflect the new logic where a missing or blank description becomes null. The change in amount from 0 to 10 makes the test more meaningful.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/54#discussion_r2431263291" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The use of @param and @return tags ensures that every aspect of the method is covered, providing concise explanations for each argument and return type. Well done!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/54#discussion_r2431265050" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The style and structure of the Javadoc comments are consistent throughout, which enhances readability and maintainability.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/104#discussion_r2462941684" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice to see a concrete responsiveness target. This gives implementers a clear UX goal and makes performance expectations testable. Good for guiding benchmarks and CI performance checks.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/104#discussion_r2462944599" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Having an explicit requirement for a comprehensive help command is excellent - it improves discoverability and lowers the barrier for new users.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/109#discussion_r2463188647" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Clear and detailed sequence diagram. Well done!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/109#discussion_r2463188892" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Javadoc is very clear and detailed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/109#discussion_r2463190474" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Love this `KNOWN_TIPS` block: it's concise, relatable and adds real personality (humorous and campus-specific) that will engage users.

Technically tidy too declared as immutable `static final`, easy to read, maintain and extend with more tips.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/109#discussion_r2463191129" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This is an excellent test suite: clear, focused tests with descriptive names that make failures easy to diagnose.

Well-structured setup and strong assertions increase confidence in the FinTrack module and reduce regression risk.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/117#discussion_r2463863857" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Detailed user profile - well done!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/117#discussion_r2463864601" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Detailed, yet succinct documentation of key features. Nicely done.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/117#discussion_r2463865024" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for updating the command table!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/131#discussion_r2464484462" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM - descriptions are highly informative and easy to understand. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/137#discussion_r2465313041" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This is an especially informative and useful output. Well done!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/137#discussion_r2465314300" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Validation notes are clear and detailed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/148#discussion_r2469544778" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for fixing my typo! :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/148#discussion_r2469549659" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Diagrams are clear and use proper CS2113 notation. Nicely done, Sanjay :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/148#discussion_r2469557207" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You have written a very clear and informative explanation of how the program works!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/171#discussion_r2477220301" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch, Sanjay! Thanks for fixing the inconsistency.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/171#discussion_r2477247129" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Indeed, an important point to note.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/167#discussion_r2483179366" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good error handling, Kenneth!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/280#discussion_r2485154194" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great! Now running tests won't produce untracked files.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/280#discussion_r2485155322" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great that you noted this - it's a limitation that's unfortunately out of scope for us.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/280#discussion_r2485157759" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good error handling!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/280#discussion_r2485158507" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice plain-text storage implementation; clear format, atomic temp-write and robust parsing.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/278#discussion_r2485293821" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great! You corrected your notation for object diagrams.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/166#discussion_r2476809399" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Yes! Have fixed this. Thanks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/166#discussion_r2476809922" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Fixed!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/98#issuecomment-3449967478" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

Closed by #133.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/198#issuecomment-3476547842" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

Unable to reproduce. Attempted to use the reported command `modify-expense 7 a/1300 c/Rent d/2024-01-01 des/Monthly rent increased` but unable to get the "Invalid command" message described.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/228#issuecomment-3477431832" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

`UiInputCycle.puml` is already accurate; no extra “:” markers are required.
                                                                                                                                                                                                         
  - Ui is never instantiated. Every interaction in `Ui.waitForInput()` is through static members, so showing it with the `&lt;&lt;static>>` stereotype (and without an instance colon) is correct UML.                                                                                                                                                           
  - The Logger used in that flow is the static field `LOGGER`. It represents a class-level singleton, which the current diagram also depicts with `&lt;&lt;static>>`.    
                                                                                                                                                                                                         
  Because there is no new `Ui()` and no per-call logger object, this report is incorrect and the diagram needs no changes.  
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/227#issuecomment-3477584911" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

Issue noted; will export in A3 size to ensure entire document is shown.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 7. VITO..ALIM `@V1T0bh` (**29** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/4#discussion_r2377919900" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Please change the display photo just incase.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/36#discussion_r2415401824" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

suggest to split based on dash rather than slash (e.g. 17-09-2025 seems more logical than 17/09/2025 when writing the command)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/56#discussion_r2426560818" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Tests are very extensive! Nice!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/66#discussion_r2445496253" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Amazingly creative command! 🤣
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463891254" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of abstraction in making printDashboard function
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463916363" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Very detailed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463916424" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463916577" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463916695" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Correctly updated
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463916789" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice catch
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463916900" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/93#discussion_r2463917254" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of code In making UML diagram
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/94#discussion_r2464464922" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice, good file change. Cool file name
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/95#discussion_r2465294218" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good use of methods
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/95#discussion_r2465295200" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

standardising outputs. Nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/125#discussion_r2478478507" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Already given under `dashboard` and `exit` sections respectively. Should this still be necessary? Or you could remove the notes from the sections cause they seem repetitive.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484777562" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch on discrepancy but I don't think it affects anything
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484779597" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484780030" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Using constants for readability. Good call.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484785457" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

add space before ``{`` for coding standard
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484785933" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could follow same parameter as printRemoveInternship. Pass in internshipInfo instead of internship so that Ui class doesnt need to get details from internship class.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484786219" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

try adding a check if a pay > MAXINT is given. see if expected output is given.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/190#discussion_r2484788400" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

mysterious `%7C` string. should maybe be defined somewhere.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/190#discussion_r2484824080" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484900423" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good fix :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/195#discussion_r2486723232" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could you save a higher res version of the diagram? Not sure how to exactly do it but re-saving it sometimes changes the resolution
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/195#discussion_r2486731265" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

`&lt;code>COMPANY_NAME&lt;&lt;/code>` extra &lt; after letter E, left there from previous commit
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/195#discussion_r2486731875" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Low res photo
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/195#discussion_r2486732286" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Low res photo
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/52#discussion_r2426417883" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thank you, I appreciate the feedback! and thank you for looking through the code!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/59#discussion_r2435386871" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

I see. I was trying to assert that IF the code reaches that line, THEN it implies that listAll ran successfully without any "code breaking" errors. In that case, is the assertion still unnecessary?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/59#discussion_r2435387459" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thank you!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/59#discussion_r2435436248" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

That makes a lot of sense. Thank you for the feedback and insights. I will amend my code ASAP.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/198#discussion_r2486911385" expanded>
<div slot="header">

**34 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

I keep forgetting, thank you for the reminder.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/57#issuecomment-3401305742" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/59#issuecomment-3410383724" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

@lukeai-tan I amended my code. Please proceed with another review. Thank you
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/78#issuecomment-3422875926" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

> Very good implementation of the sorting method. Just a few coding standard hiccups and redundancies to look into.

Thanks for the feedback! I have amended the code to reflect these changes. I hope it looks fine now
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/106#issuecomment-3460195149" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

my bad i was closing my PR so it doesnt get prematurely pushed. Ready to review now!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/170#issuecomment-3476026275" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

Help shows:
```
list      : Display all internship applications, optionally sorted by deadline.
```

invalid list command shows
```
Usage: list [sort/asc|sort/desc]
```

Both are already consistent as they show the optional use of sorting
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/168#issuecomment-3476029585" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

similar to #171 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/167#issuecomment-3476032197" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

related to #172 (can be fixed concurrently)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/166#issuecomment-3476033811" expanded>
<div slot="header">

**42 :octicon-comment:** %%(other comment)%%
</div>

similar found #172 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/165#issuecomment-3476035156" expanded>
<div slot="header">

**43 :octicon-comment:** %%(other comment)%%
</div>

similar found
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/164#issuecomment-3476036105" expanded>
<div slot="header">

**44 :octicon-comment:** %%(other comment)%%
</div>

format given in instructions wrong! `expected == actual`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/158#issuecomment-3476040155" expanded>
<div slot="header">

**45 :octicon-comment:** %%(other comment)%%
</div>

related to #159  (can fix together)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/156#issuecomment-3476057742" expanded>
<div slot="header">

**46 :octicon-comment:** %%(other comment)%%
</div>

#173 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/153#issuecomment-3476060766" expanded>
<div slot="header">

**47 :octicon-comment:** %%(other comment)%%
</div>

#173 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/152#issuecomment-3476061645" expanded>
<div slot="header">

**48 :octicon-comment:** %%(other comment)%%
</div>

#173 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/151#issuecomment-3476065515" expanded>
<div slot="header">

**49 :octicon-comment:** %%(other comment)%%
</div>

related to #149

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/150#issuecomment-3476070960" expanded>
<div slot="header">

**50 :octicon-comment:** %%(other comment)%%
</div>

bug invalid: corrupted fields/records in internships.txt are announced at the start of program

Example:

```
Warning: Skipped line with invalid pay format: microsoft | Janitor | 10-10-2025 | ten thousand | Pending

```
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/148#issuecomment-3476078698" expanded>
<div slot="header">

**51 :octicon-comment:** %%(other comment)%%
</div>

should this be fixed?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/147#issuecomment-3476082756" expanded>
<div slot="header">

**52 :octicon-comment:** %%(other comment)%%
</div>

related to #149 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/146#issuecomment-3476086453" expanded>
<div slot="header">

**53 :octicon-comment:** %%(other comment)%%
</div>

related to #163 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/144#issuecomment-3476089782" expanded>
<div slot="header">

**54 :octicon-comment:** %%(other comment)%%
</div>

related to #172 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/143#issuecomment-3476090619" expanded>
<div slot="header">

**55 :octicon-comment:** %%(other comment)%%
</div>

related to #148 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/142#issuecomment-3476091014" expanded>
<div slot="header">

**56 :octicon-comment:** %%(other comment)%%
</div>

time travel is possible if you believe
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/142#issuecomment-3476091496" expanded>
<div slot="header">

**57 :octicon-comment:** %%(other comment)%%
</div>

could be related to #152 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/154#issuecomment-3476096578" expanded>
<div slot="header">

**58 :octicon-comment:** %%(other comment)%%
</div>

activation bar may be omitted as long as consistent within same diagram. - prof akshay
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/141#issuecomment-3476097187" expanded>
<div slot="header">

**59 :octicon-comment:** %%(other comment)%%
</div>

related to one I could not find
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/137#issuecomment-3476099082" expanded>
<div slot="header">

**60 :octicon-comment:** %%(other comment)%%
</div>

related to #167, #172
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/135#issuecomment-3476100361" expanded>
<div slot="header">

**61 :octicon-comment:** %%(other comment)%%
</div>

solved by #173 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/134#issuecomment-3476101146" expanded>
<div slot="header">

**62 :octicon-comment:** %%(other comment)%%
</div>

solved by #173 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/132#issuecomment-3476102581" expanded>
<div slot="header">

**63 :octicon-comment:** %%(other comment)%%
</div>

related to #132
solved by #173 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/131#issuecomment-3476103549" expanded>
<div slot="header">

**64 :octicon-comment:** %%(other comment)%%
</div>

may be redundant
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/130#issuecomment-3476104057" expanded>
<div slot="header">

**65 :octicon-comment:** %%(other comment)%%
</div>

related to #140
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/129#issuecomment-3476105666" expanded>
<div slot="header">

**66 :octicon-comment:** %%(other comment)%%
</div>

time travel again
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/129#issuecomment-3476106186" expanded>
<div slot="header">

**67 :octicon-comment:** %%(other comment)%%
</div>

may be related to #152, #142
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/128#issuecomment-3476107331" expanded>
<div slot="header">

**68 :octicon-comment:** %%(other comment)%%
</div>

list sort by other things (not just deadline).... but is this a bug???
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/127#issuecomment-3476114576" expanded>
<div slot="header">

**69 :octicon-comment:** %%(other comment)%%
</div>

related to #138
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/173#issuecomment-3477917962" expanded>
<div slot="header">

**70 :octicon-comment:** %%(other comment)%%
</div>

acknowledged and resolved changes @lukeai-tan 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/129#issuecomment-3481468918" expanded>
<div slot="header">

**71 :octicon-comment:** %%(other comment)%%
</div>

closed. our app allows users to add deadlines that come before the current date.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/128#issuecomment-3481482012" expanded>
<div slot="header">

**72 :octicon-comment:** %%(other comment)%%
</div>

related to #136 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/136#issuecomment-3481482925" expanded>
<div slot="header">

**73 :octicon-comment:** %%(other comment)%%
</div>

partially solved by #194 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/158#issuecomment-3481511281" expanded>
<div slot="header">

**74 :octicon-comment:** %%(other comment)%%
</div>

solved by #175 

only ascii character allowed
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 8. ZHU ..ENBO `@mendax1234` (**28** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/27#discussion_r2374807930" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

There is no need to create a Timetable in the electivecommand, as there is one called `data` in its parent class -- `Command`, can just call `data.methodName()` to add the module into the correct place
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/27#discussion_r2374813333" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can encapsulate this code into a method? Like what is alr done for the helpCommand.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/27#discussion_r2374816017" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Correct observation! Thanks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/27#discussion_r2374828075" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

semester can be changed to term for better clarity, this convention is used in our timetable also
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377886705" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Use an import statement to import the Module here.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377891910" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe can have a better name for this method cuz it actually parses eahc input line and it should ruturn a List&lt;Module> instead of being void.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377894481" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

There shouldn't be a ModuleList field inside Storage. Instead, make the `loadAllModules()` (old name) to return `ModuleList` instead of `void`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377899564" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

`storage` shouldn't be passed to the command. In other words, should here the command should only receive electiveList and coreList, even the timetable is no need. As I think all our commands only manipulate on the electiveList and coreList and our timetable will deal with the converion from elective list and core list into the timetable output. But if doing so, we may need to make the `printTimetable()` in the `Timetable.java` to be a class method instead of an instance method.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377904347" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

the `String` argument to initialize `Storage` should be the path to our txt files, e.g., `./data/data.txt` (`.` means the data file starts searching from the same path as where you execute ur java program)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377905430" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

As explained before, don't need `Storage` field inside the command
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377905811" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe for the `Timetable` also don't need
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377907410" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Delete can only delete from elective list and cannot delete from core list. Good but we need to discuss this feature in the grp meeting later.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377909401" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

we shouldn't call any method from the `Storage` and also our storage shouldn't provide this method because `Storage` only account for loading and saving. Instead, the find ModuleByCode should be done in the `ModuleList.java`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2377911045" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job for pointing this out!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2383963622" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think `allModules` should be stored elsewhere other than in the `Storage` class. Maybe in the `Timetable` cuz using the `has-a` relationship introduced by `composition`, I think the Timetable should have a `ModuleList` called `allModules` list.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2383964201" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think maybe the naming of `allModules` should be changed to something else for better clarity, cuz it either loads core modules or elective modules.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2383964630" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe we should change `List&lt;String>` to `ModuleList` to make the code coherent.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2383964834" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Here for the electives, also change it to `ModuleList` instead of `List&lt;String>`.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/37#discussion_r2383966166" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

As hashmap is used to store our local lut (look up table), I think it shouldn't be stored in the `ModuleList` class, instead, it should be stored in a new Class
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/44#discussion_r2396455119" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good to be merged!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/96#discussion_r2462884608" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Why do u delete the initializeData()? It should be there to initialize the data
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/96#discussion_r2462885004" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Code quality issue here, whitespace after ```}```
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/101#discussion_r2463200311" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think this shouldn't be static
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/101#discussion_r2463200559" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Shouldn't call the class method here.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/104#discussion_r2463769281" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

What's the point of these two methods?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/104#discussion_r2463769720" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This error shouldn't be thrown here. We deal with all the error regarding the delete command in `DeleteCommand.java`. Not in `Timetable.java`.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/104#discussion_r2463769992" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe can put this exception into command. Because all the classes in `common` are going to be used by other modules wheras this module is not used by other classes for now
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/104#discussion_r2463770441" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Delete module should check the rest of the modules still meet the prerequisite or not. But here I cannot find such case. Also the exception handling is not here also.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/4#issuecomment-3322579933" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

@HiewTheG Next time can create a PR next time instead of changing directly at the master branch. Thanks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/76#issuecomment-3420456907" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Does this compile? Cuz I see @AWeiBin has already done a PR for the NUSMODS, so would you mind providing more details on what did you add? Or what did you do in the newer code? Thanks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/77#issuecomment-3424706217" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

@AWeiBin I have fixed as you required! Please take a look again! And let me know if have any other problems!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/80#issuecomment-3446580153" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

Got conflicts this pr, either resolve it or close . @AY2526S1-CS2113-T10-4/developers 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/76#issuecomment-3446580572" expanded>
<div slot="header">

**33 :octicon-comment:** %%(other comment)%%
</div>

@AY2526S1-CS2113-T10-4/developers is this still in active ? If not, will just close it?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/12#issuecomment-3448586658" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

Close as this won't be implemented.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/59#issuecomment-3448586787" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

Close as this won't be implemented.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/52#issuecomment-3448588180" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

Close as this won't be implemented
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/58#issuecomment-3448588263" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

Close as finished
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/55#issuecomment-3448588529" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

Close as finished
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/51#issuecomment-3448588794" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

Close as finished
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/57#issuecomment-3448589113" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

Close as finished
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/120#issuecomment-3456169653" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

Closes as finish #119 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 9. SANJ..UMAR `@sanjay-shiva-kumar` (**27** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/48#discussion_r2423456830" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you separated the logging into appropriate levels for each situation. Great job!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/48#discussion_r2423458050" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you accounted for different edge-cases for the assertions :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/68#discussion_r2445326214" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you accounted for many different edge-cases using exceptions!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/68#discussion_r2445333443" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you used the Ui variables to break this up neatly!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/84#discussion_r2454920970" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like your clear explanations for how the various classes perform certain features!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/84#discussion_r2454923954" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you added sequence diagrams for clarity!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/87#discussion_r2455295532" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like the level of detail of the error messages!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/87#discussion_r2455298428" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you stress test specific functions in the class.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/97#discussion_r2462684183" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good JUnit tests!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/97#discussion_r2462684315" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good tips for NUS CEG students!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/123#discussion_r2463920301" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good table formatting!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/123#discussion_r2463920526" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

it makes sense that income should have an OTHERS category just like expense!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/126#discussion_r2463921167" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

very nice class diagram!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/126#discussion_r2463921250" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

very nice class diagram!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/126#discussion_r2463921399" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

its good that you added the .puml code of each diagram as well!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/139#discussion_r2465855410" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Descriptive and clear steps!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/141#discussion_r2465859924" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for all your hard work, Kenneth "duckyfuz" Gao!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/166#discussion_r2476631716" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Shouldn't Ui also be shown as static?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/166#discussion_r2476632630" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same here, shouldn't Ui be static?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/170#discussion_r2477061048" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good to replace with an informative comment instead of just deleting.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/166#discussion_r2477157544" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This is a more clear sequence diagram, omitting unnecessary details.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/237#discussion_r2483772719" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

These instructions are more comprehensive!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/241#discussion_r2483780553" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This is a great overhaul of our parsing system! This will make it much more reliable!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/241#discussion_r2483780997" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

It's great that you added a specific error message for this error!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/245#discussion_r2483810124" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

These updates to our documentation definitely help to cover our bases!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/283#discussion_r2485278574" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good that we differentiate these errors! Its a subtle difference but a difference nonetheless.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/298#discussion_r2487443474" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good clarification!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/28#issuecomment-3378082496" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

Reopening — I’ll be implementing this story as discussed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/48#issuecomment-3394114226" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/135#issuecomment-3449972199" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Thank you for changing for everyone!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/231#issuecomment-3476438170" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

We (the FinTrack dev team) have decided that inputting future expenses and incomes are valid, and it is up to the user to decide if they want to do so or not. For example, it may be helpful for a user to pre-emptively log expenses/incomes that they know will occur at regular intervals.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/196#issuecomment-3476438467" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

We (the FinTrack dev team) have decided that inputting future expenses and incomes are valid, and it is up to the user to decide if they want to do so or not. For example, it may be helpful for a user to pre-emptively log expenses/incomes that they know will occur at regular intervals.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/issues/209#issuecomment-3476438927" expanded>
<div slot="header">

**33 :octicon-comment:** %%(other comment)%%
</div>

We (the FinTrack dev team) have decided that inputting future expenses and incomes are valid, and it is up to the user to decide if they want to do so or not. For example, it may be helpful for a user to pre-emptively log expenses/incomes that they know will occur at regular intervals.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/236#issuecomment-3476460748" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/242#issuecomment-3476537028" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

LGTM! This change definitely improves the separation of concerns of our app!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/244#issuecomment-3476555210" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

LGTM! This change helps align valid behaviour throughout the entire program!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/245#issuecomment-3476612922" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/271#issuecomment-3477970346" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

PR #273 fixes this issue :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/268#issuecomment-3478094070" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

LGTM! Thank you for doing due diligence to adhere to UML standards!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/299#issuecomment-3481972681" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 10. NGUY..LOAN `@bennyy117` (**27** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/51#discussion_r2426380655" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice use of constants for ANSI color codes! It keeps the code organized and readable.
However, should these be grouped or documented (e.g., as a small enum or inner class like TextColor) for easier maintenance if you add more color codes later?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/51#discussion_r2426383075" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you used color to make the prompt stand out!
Would it be useful to handle empty input (e.g., if the user just presses Enter)? Maybe return a default message or re-prompt?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/62#discussion_r2428430239" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider capturing color codes in tests more explicitly. Right now, showMessage checks for the reset code \u001B[0m. It might be good to also verify the color prefix code (if your UI uses one like \u001B[32m for green text).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/72#discussion_r2429429488" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/72#discussion_r2429430160" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/121#discussion_r2451784713" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/124#discussion_r2452039340" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/124#discussion_r2452039933" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice color
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/128#discussion_r2454393419" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/145#discussion_r2459114497" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

necessary
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/159#discussion_r2462959360" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

looks nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/159#discussion_r2462959475" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/182#discussion_r2468762494" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice icon
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/182#discussion_r2468764308" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

necessary
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/182#discussion_r2468765543" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good change
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/186#discussion_r2470685930" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice format
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/201#discussion_r2476507125" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thanks for let it be clear
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/204#discussion_r2477005737" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

is it in wrong format?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/204#discussion_r2477008216" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice addition
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/198#discussion_r2478151610" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

necessary change
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/257#discussion_r2483763732" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thanks for updating format
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/257#discussion_r2483764369" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

necessary change
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/270#discussion_r2484276863" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

easier to understand
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/288#discussion_r2487437919" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/289#discussion_r2487613769" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good format
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/293#discussion_r2488387461" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

necessary change
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/297#discussion_r2488579011" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thanks
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 11. RAJA..THIK `@Kart04` (**26** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/57#discussion_r2426966982" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Well done in removing a dependency 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/60#discussion_r2427906914" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of Junit testing
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/87#discussion_r2438048172" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/98#discussion_r2445349087" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/100#discussion_r2445350655" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/133#discussion_r2455344849" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The use of a LinkedHashMap here to store the latest WeightRecord per day is efficient and maintains insertion order, which is important for chronological data presentation.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/133#discussion_r2455347328" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The use of assert statements here is appropriate for internal consistency checks and documenting assumptions during development.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/133#discussion_r2455351283" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

this pattern promotes clear, user-friendly validation and robust date/time parsing using the modern Java Time API as per best practices.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/164#discussion_r2463154115" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/164#discussion_r2463154267" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good idea of checking if the date is from the future.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/256#discussion_r2483721138" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good addition of shortcut for remove, will be a lot easier to use that command
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/256#discussion_r2483721249" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485356115" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you ensured that the exception handling block now only catches IndexOutOfBoundsException, which helps clarify what errors are expected in this section.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485357629" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like meticulous input validation and user-friendly error messages in parseYearMonthTokenStrict make the parser robust against malformed tokens, which is a strong point for reliability.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485359113" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how the parser gives clear, actionable error messages and usage instructions to guide users, which aligns well with robust command-line argument handling practices. Including help text in exception messages is user-friendly and makes debugging easier.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485360235" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485366134" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how the execute method handles the full delete flow end-to-end: parsing arguments, loading data, validating input, requesting user confirmation, and persisting changes. The clear messaging guides the user smoothly in CLI context.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485367344" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like the refactor towards using parseYearMonthToken(t.substring(3)), which likely encapsulates year/month parsing more neatly and improves readability by abstracting away the individual readIntArg and validation steps.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485378082" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I see that you have changed the year range from current year till 2099. Any reason for switching the validation range from to this?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/272#discussion_r2485379416" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like how you have created a Junit for DeleteWorkoutTest.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/277#discussion_r2486348333" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/282#discussion_r2487209759" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/283#discussion_r2487275940" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good update of architecture diagram
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/284#discussion_r2487299294" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/298#discussion_r2488576239" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for modifying this.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/298#discussion_r2488576353" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 12. GOH ..LING `@gohjieling834` (**24** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/29#discussion_r2414189091" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

should avoid using '*' for imports and explicitly state the imports.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/38#discussion_r2428624790" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think you can just do 'p.valid = false' and return p, since the index given is already invalid.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/38#discussion_r2428651751" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe you can consider changing the variable names to isBadIndex, hasName, hasIndex, so that they sound like boolean variables.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/38#discussion_r2428667059" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same as the comment in MarkTreatmentCommand.java
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/38#discussion_r2428667473" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same as the comment in MarkTreatmentCommand.java
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/38#discussion_r2429417525" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

sorry, i clicked on the wrong line. I meant to click on line 116, i was referring to the badIndexFormat variable.

If you do change it to 'p.valid = false', then i think you can just remove the badIndexFormat variable.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/41#discussion_r2429531499" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Printing error messages here instead of using assertions would be better, since these errors come from the user's input, and if assertions are disabled, they wouldn't be caught.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/50#discussion_r2432544175" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe you can set the level to 'severe' instead, since the user input errors are set at 'warning'. That way, they won't show up twice (logging and sout).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/67#discussion_r2436747528" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think you can consider changing this to just "enableAssertions = true", it's how they recommend doing in the course website. If you do it that way then you wouldn't need line 48 and line 34. But it's okay if you want to leave it like that too :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/68#discussion_r2436801906" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like that you used a constant for the command syntax!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/79#discussion_r2446949091" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

"hasAnyTreatments" might be a better variable name to show that you are checking if there's any treatments logged. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/79#discussion_r2447237944" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Adding on to the above comment, for this method, i think you could just return the pets attribute and it would be implicitly upcasted as List type. Then the for loop wouldn't be needed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/100#discussion_r2463883887" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The stream logic looks a bit complicated, and the overdue conditions are being repeated. Perhaps you can simplify it by extracting the filtering into a helper method that returns each pet’s list of overdue treatments, then filtering out pets with empty lists.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/100#discussion_r2463889821" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe you can try flattening this to avoid arrowhead style code. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/122#discussion_r2473363956" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This method is too long, consider extracting some code out into a separate method and call those methods in here.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/124#discussion_r2477592112" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

there's a printHeader method in the Ui class
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/124#discussion_r2477600866" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I don't think this method is used at all, so maybe you can remove it.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/233#discussion_r2486315698" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

there's a typo error, "species" is missing "s"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/233#discussion_r2486320610" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

there's a typo error here too, "part" --> "past"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/233#discussion_r2486322115" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same typo as the add pet
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/249#discussion_r2488364952" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

max pet age is 200 years
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/249#discussion_r2488365737" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

can just use the printInvalidInputMessage in the Ui class, same for delete-pet
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/249#discussion_r2488379911" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

also remember to add validation for the name and species max characters.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/249#discussion_r2488478195" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Ui is a static class, would be better to represent it as `"&lt;&lt;class>>\nUi"` instead.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 13. RYAN..GKAI `@goodguyryan` (**24** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/41#discussion_r2422805173" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good choice to ensure that the CLI does not get flooded with log information so the users are still able to view the CLI properly!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/41#discussion_r2422808169" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can consider dropping info logs but good to have during development stage
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/41#discussion_r2422808881" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of assertion to ensure input is not null
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/62#discussion_r2442456911" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for updating the tests as well!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/62#discussion_r2442457116" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good idea on showing what the available categories are.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/62#discussion_r2442457336" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice budget Ui
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/62#discussion_r2442457513" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good error checking!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/62#discussion_r2442458389" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of abstraction!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/75#discussion_r2448971485" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for updating the expected text!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/75#discussion_r2448972577" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good attempt of trying to handle home directory
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/75#discussion_r2448973522" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good error checking!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/80#discussion_r2454126314" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thank you for updating the test as well!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/80#discussion_r2454127257" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good error handling!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/91#discussion_r2459040308" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for updating the User Stories as well!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/91#discussion_r2459041939" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

very nice diagrams!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/93#discussion_r2459057122" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good documentation!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/93#discussion_r2459057441" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

very nice diagram!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/107#discussion_r2462971516" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for updating the README as well!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/107#discussion_r2462971759" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for all your hard work for tp!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/110#discussion_r2463216292" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Very good description!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/121#discussion_r2463903882" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for all your hard work Jordan!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/133#discussion_r2464486402" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for writing this test!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/133#discussion_r2464488515" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good error checking!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/133#discussion_r2464488854" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thank you for updating the tests!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/19#issuecomment-3370514262" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/38#issuecomment-3380409577" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/41#issuecomment-3393296672" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/74#issuecomment-3427585353" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

So far it looks good! Try to give your parameters more meaningful names and remember to resolve the merge conflict!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/106#issuecomment-3446975101" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/150#issuecomment-3461230144" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/162#issuecomment-3462962061" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-4/tp/pull/168#issuecomment-3466491095" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 14. RAYA..WONG `@Rayan-Wong` (**22** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/20#discussion_r2417002947" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Dont forget newline them later or smth
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422535959" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can you make these as a toString() method
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/28#discussion_r2424503355" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Why's the constructor defined before another variable?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/29#discussion_r2425016665" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Shouldn't this be onReminder?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/51#discussion_r2464262327" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nicely done adding a table of user stories done!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/51#discussion_r2464263158" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice attention to detail!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/51#discussion_r2464263588" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice job testing the hi and bye messages!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/49#discussion_r2464268493" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Did we need a separate class just to show the indexes when printing?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/49#discussion_r2464269067" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Do these follow the style guide?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/44#discussion_r2464269762" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

It was good to make the Task abstract to reflect it is not a concrete implementation
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/42#discussion_r2464271014" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job adhering to the style guide!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/39#discussion_r2464272270" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I appreciate making the parse interval function a separate method for other future methods to use!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/65#discussion_r2469085041" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Overall clear explanations given for DG!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/67#discussion_r2469796897" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like the tables showing how the other components are integrated
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/69#discussion_r2470519855" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Very clear conditions stated for loop and alt
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/69#discussion_r2470525388" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Very clear relationships!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/69#discussion_r2470526577" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice touch on adding purpose of the classes
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/69#discussion_r2470533466" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should we be using composition between Task and TaskList instead of aggregation? Interactions with Tasks are done through TaskList
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/70#discussion_r2471503933" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch on formatting how seconds are displayed for the timer!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/159#discussion_r2484913793" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Do we need this method in ReminderList?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/167#discussion_r2487327547" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good effort in cleaning up comments!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/167#discussion_r2487328018" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for clarifying test purposes!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/103#issuecomment-3475376615" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Duplicate issue of #98 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/107#issuecomment-3475378732" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Duplicate issue of #90 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/109#issuecomment-3475379474" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

Duplicate issue of #99
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/110#issuecomment-3475380980" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

Note: Just accept we cannot fulfill 3 as PlantUML doesnt let us change that
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/112#issuecomment-3475382225" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #91
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/113#issuecomment-3475385319" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #99 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/115#issuecomment-3475386135" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

Out of spec and duplicate with #99
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/116#issuecomment-3475386807" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Note: Just put in FAQ of UG why we use that special delimiter
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/117#issuecomment-3475387490" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #98
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/119#issuecomment-3475388717" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #110
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/125#issuecomment-3475391814" expanded>
<div slot="header">

**33 :octicon-comment:** %%(other comment)%%
</div>

Note: Just say in UG if only numbers are given the start command will try to parse it as a index no matter what

Basically, user fault

Also emphasise first arg will never be treated as time
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/92#issuecomment-3475422609" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

Note: Can also just admit it is a limitation rn in FAQ section and post v2.1 we fix it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/116#issuecomment-3475727982" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

Duplicate
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/106#issuecomment-3475728177" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

Note: Just put in FAQ of UG why we use that special delimiter
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/89#issuecomment-3475953411" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

To note: current fix needs us to highlight in UG/DG we cant search by datetimes anymore
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/124#issuecomment-3476616809" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

Could also just acknowledge as documentation it is a known bug
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/95#issuecomment-3477451459" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

Just highlight in UG the program treats it as if the reminder is off and the time for it to trigger has past, the program assumes the user does not want the reminder anymore and so will never trigger it again
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/issues/93#issuecomment-3477502876" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #114
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 15. ROYD.. REN `@roydenlyr` (**20** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/13#discussion_r2396463249" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

put you full name please
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/15#discussion_r2396468331" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/17#discussion_r2416284087" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps this can be shortened? something like outputString += (isRepaid ? "repaid" : "outstanding");
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/17#discussion_r2416288956" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps can utilise StringBuilder instead of String for string concatenation?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/17#discussion_r2416294032" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

What if instead of overriding, super(message) is used instead? Would that be "cleaner"?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/17#discussion_r2416325440" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Is numberOfLoans neccessary? Would loans.size() achieve the same result?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/17#discussion_r2416331738" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nitpicking here but would it be better if setRepaid takes in a boolean argument instead?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/24#discussion_r2432040956" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

what if investmentDate falls on months where there is only 28-30 days?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/24#discussion_r2432046617" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Very descriptive error messages. Good Job!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/24#discussion_r2432053565" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good work changing input to lowercase!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/24#discussion_r2432067393" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would it be better if data type is LocalDate or equivalent?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/29#discussion_r2438736494" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good Job for abstracting this from Parser!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/51#discussion_r2447789772" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/85#discussion_r2469762017" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

should writeToFile() be included?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/100#discussion_r2472599180" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

😘Good Job starting on them first
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/114#discussion_r2478998989" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job figuring out the work around!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/172#discussion_r2483790465" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

isn't this a feature and not a bug? IP has the same thing of converting date format too
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/172#discussion_r2483792106" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would 1 cent already indicate its a float?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/172#discussion_r2483792713" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job adding test case for new feature
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/174#discussion_r2484698839" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good catch
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 16. LEE ..HENG `@Lee-YiSheng` (**19** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/8#discussion_r2400946865" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Create issue for class MAMA and PR it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/8#discussion_r2400947867" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

PR interface Command separately, with an issue to track it.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/8#discussion_r2400948341" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

PR class Parser separately with an issue to track it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/8#discussion_r2400949665" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

PR Storage class separately and track it as an issue
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/47#discussion_r2419130654" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Add newline to pass the EXPECTED test
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/47#discussion_r2419139722" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Add newline at all java files
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/47#discussion_r2419140096" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Add newline at all java files
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/56#discussion_r2430919717" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good wrapping which preserves the stack trace of the original error and makes debugging easier
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/56#discussion_r2430925506" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The execute method is currently handling validation, deletion, persistence, logging, and message formatting all in one place. This makes it quite long and mixes different levels of abstraction (violating SRP and SLAP). In future, we could refactor by:
Extracting previewList into a utility/Ui class (so commands don’t handle formatting).
Moving persistence error handling into a helper method to shorten execute.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/56#discussion_r2430926234" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could this be extracted into a utility/Ui class (so commands don’t handle formatting)?

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/77#discussion_r2450217924" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good naming, it is clear of what it is (a feedback) and who is it for (user)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/87#discussion_r2450885761" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good naming convention, adheres to class noun principles and clarifies what does it do (a milk adder)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/88#discussion_r2451011905" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

May be good to refactor to BodyMeasurements class (to encapsulate waist/hips/chest/etc.) in the future.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/88#discussion_r2451022845" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should this be wrapped into measurementCommandParser class in the future? 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/106#discussion_r2468464967" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should this be removed?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/106#discussion_r2468473026" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

please redact this, the main should use the new Ui instead of the old one.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/106#discussion_r2468475831" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good naming convention to indicate the Command's functionality!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/188#discussion_r2484566304" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

should this be redacted to prevent calorie goal from showing up on list?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/193#discussion_r2484760192" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

should comments like this stay in the code?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/13#issuecomment-3364523536" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

Remember to label, tag, milestone, and assign the issue to yourself.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/12#issuecomment-3364559720" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

For Sub tasks, try to tag it to the main story as sub-issues and follow standard format of e.g., 
[Parser] Implement Commands

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/1#issuecomment-3394088399" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

Is this resolved yet?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/33#issuecomment-3394089029" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Is this resolved? link to Add workout v1 #34

</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 17. TAN .. JIE `@zhengjie2002` (**17** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/8#discussion_r2403669213" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nit: Perhaps you can consider renaming this method as it is not very obvious from the name that is parses and executes the command?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/9#discussion_r2403672561" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should case files be in another package instead of the utility package since it is the domain object?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/9#discussion_r2403674947" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps we can make this method `private`?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/11#discussion_r2403676944" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would it be better if we create a private attribute called `commandType` in the `Command` class and use the getter to retrieve the `commandType` instead of just returning the CommandType?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/11#discussion_r2403679616" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nit: Perhaps you can consider extracting the strings out to avoid magic literals?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/50#discussion_r2426530025" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you can use a constant here to avoid magic string literals?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/50#discussion_r2426530835" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you can add a Javadoc for this method to explain how this method can be used.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/80#discussion_r2441831609" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you can consider editing this to use the automatic line break function that @xelisce created.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/80#discussion_r2441842984" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider moving all the display operation to the `execute` method to keep the CaseManager class only responsible for managing cases. Maybe we can throw error and catch them in the execute class.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/80#discussion_r2441850391" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you can move this to the validator class to follow the other commands.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/130#discussion_r2462924282" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps we can consider storing these as integer data type for data integrity purpose, and perform validation to ensure it is a valid positive int.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/130#discussion_r2462924613" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you can consider using dash-case instead of camelCase for command line flags as it is more conventional
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/130#discussion_r2462924931" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider adding comments on exception thrown (Can refer to other javadoc comments for reference)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/130#discussion_r2462932561" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This is unsafe as return value of getInvalidFlags() might be null given that invalidFlags in IncorrectFlagException is instantiated as null (although this shouldn't happen if execution is correct, but there is a risk)

Perhaps you can perform a null check before using the flag.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/130#discussion_r2462933293" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think this should be part of validator instead of CaseManager
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/130#discussion_r2462945000" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think the happy path will also not throw any exception so the test doesn't determine if case is not found. Perhaps you might want to get the print into a ByteArrayOutputStream and assert the equivalence.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/151#discussion_r2467569888" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think this can be extracted out as a static variable to avoid magic string literals.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/18#discussion_r2412674814" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Good suggestion, I will add a comment to make it clearer for future developers. 👍 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/18#discussion_r2413581226" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

I''ve abstracted some parts of the function to make it more readable.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/15#issuecomment-3379225619" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

The following will be done to fulfil this user story
- [x] Add the `add` functionality to allow the user to add cases and fill in the details
- [x] Handle error when user input inaccurate command (e.g., missing of compulsory input flags)
- [x] JUnit test for the above functionality
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/67#issuecomment-3411224411" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

PR causes breaking change, thus it will be merged into a new branch instead of master to maintain master as production ready. This PR will be closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/72#issuecomment-3424443351" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

Fixed in #89 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/92#issuecomment-3424992422" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Closed by PR #93 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/216#issuecomment-3475835011" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

The ID field is considered as unique, not null fields. Due to implementation of soft deletion, the suggestion is not possible. However, we can state this in DG as NFR and assumption. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/217#issuecomment-3475843051" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

To implement error handling for different data type
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/218#issuecomment-3475844200" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

Display issue with UG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/219#issuecomment-3475905434" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

Similar suggest as #220  @xelisce for your consideration
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/223#issuecomment-3475905887" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

Worthy change
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/224#issuecomment-3475906333" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

I think we can make this change (although not compulsory) so that such bugs will not be repeated in PE.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/228#issuecomment-3475909581" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Similar suggestion as #224 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/227#issuecomment-3475910034" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

Interesting finding, will need more time to triage to find out the root cause.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/229#issuecomment-3475910812" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

Will implement in v2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/231#issuecomment-3475911428" expanded>
<div slot="header">

**33 :octicon-comment:** %%(other comment)%%
</div>

@limeiy1 for your consideration to see if the reported DG bug is accurate
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/232#issuecomment-3475911734" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

To be added in UG for v2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/233#issuecomment-3475913540" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

Data persistence NFR is relevant and implemented in the current system already, will update that in the DG. However security NFR is not easily implementable and will be considered as 'Not in scope'
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/235#issuecomment-3475914304" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

Good consideration. I think we might need to implement better validation for data reading. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/236#issuecomment-3475915525" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

Interesting suggestion, will be explored if there is time as a data validation mechanism.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/237#issuecomment-3475919115" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

It is not included in the add command to prevent the add command for being extremely long and hard to type. This 2 step process is intentional. However, agreed that this can be better stated in the UG for clarity.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/238#issuecomment-3475923193" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

User have been mistaken by the UG as the instructions in the UG are just "examples". However, phrasing in UG can be improved for better clarity.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/239#issuecomment-3475927778" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

Issue is not relevant as it was routed to the wrong project.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/240#issuecomment-3475932886" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

Minor UG bug to be fixed in V2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/241#issuecomment-3475938601" expanded>
<div slot="header">

**42 :octicon-comment:** %%(other comment)%%
</div>

Similar to #235 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/242#issuecomment-3475939138" expanded>
<div slot="header">

**43 :octicon-comment:** %%(other comment)%%
</div>

Issue is not relevant as it was routed to the wrong project.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/245#issuecomment-3475940443" expanded>
<div slot="header">

**44 :octicon-comment:** %%(other comment)%%
</div>

Typographical error to be fixed by v2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/246#issuecomment-3475940506" expanded>
<div slot="header">

**45 :octicon-comment:** %%(other comment)%%
</div>

Issue is not relevant as it was routed to the wrong project.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/247#issuecomment-3475941740" expanded>
<div slot="header">

**46 :octicon-comment:** %%(other comment)%%
</div>

@limeiy1 For your consideration. Personally, I feel might not be suitable to have it in all case categories as that field is not relevant for all but the naming conventions can be standardised.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/248#issuecomment-3475942570" expanded>
<div slot="header">

**47 :octicon-comment:** %%(other comment)%%
</div>

Similar to #222 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/249#issuecomment-3475943244" expanded>
<div slot="header">

**48 :octicon-comment:** %%(other comment)%%
</div>

To triage the issue and attempt a fix in V2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/250#issuecomment-3475943520" expanded>
<div slot="header">

**49 :octicon-comment:** %%(other comment)%%
</div>

Formatting error in UG, to be fixed in V2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/251#issuecomment-3475943875" expanded>
<div slot="header">

**50 :octicon-comment:** %%(other comment)%%
</div>

To be fixed in V2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/252#issuecomment-3475951688" expanded>
<div slot="header">

**51 :octicon-comment:** %%(other comment)%%
</div>

Might be useful to improve phrasing in UG to prevent such bugs
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/256#issuecomment-3475953651" expanded>
<div slot="header">

**52 :octicon-comment:** %%(other comment)%%
</div>

Similar to #229 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/259#issuecomment-3475955395" expanded>
<div slot="header">

**53 :octicon-comment:** %%(other comment)%%
</div>

To be fixed in V2.1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/260#issuecomment-3475956009" expanded>
<div slot="header">

**54 :octicon-comment:** %%(other comment)%%
</div>

This is due to limitation of PlantUML and the issue have been stated as a footnote in the DG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/261#issuecomment-3475958803" expanded>
<div slot="header">

**55 :octicon-comment:** %%(other comment)%%
</div>

No issue mentioned
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/263#issuecomment-3475960769" expanded>
<div slot="header">

**56 :octicon-comment:** %%(other comment)%%
</div>

Agreed, will be broken down into multiple images
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/264#issuecomment-3475961939" expanded>
<div slot="header">

**57 :octicon-comment:** %%(other comment)%%
</div>

Validation error handling
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/265#issuecomment-3475962458" expanded>
<div slot="header">

**58 :octicon-comment:** %%(other comment)%%
</div>

@xelisce For you to decide if this is a bug
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/221#issuecomment-3477345912" expanded>
<div slot="header">

**59 :octicon-comment:** %%(other comment)%%
</div>

@Michael-Low Can you see how this can be saved in the data.txt file?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/236#issuecomment-3477990051" expanded>
<div slot="header">

**60 :octicon-comment:** %%(other comment)%%
</div>

This will be considered out of scope for this project and the data validation will stop at the verification of data type (i.e., date)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/281#issuecomment-3478648190" expanded>
<div slot="header">

**61 :octicon-comment:** %%(other comment)%%
</div>

Do not merge this yet, apologies. Pending @Michael-Low to check if non-english character works with storage module.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/281#issuecomment-3483306428" expanded>
<div slot="header">

**62 :octicon-comment:** %%(other comment)%%
</div>

We have decided not to implement this fix to allow for user to have flexibility in their use. However, we will state this potential issue with a warning. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/213#issuecomment-3483686736" expanded>
<div slot="header">

**63 :octicon-comment:** %%(other comment)%%
</div>

Fixed in v2.1, thank you for the good suggestions and feedback!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 18. EMAN.. YUE `@Emannuel-Tan` (**17** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/14#discussion_r2396462794" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Please change to use your full name
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/20#discussion_r2426241442" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should this be refactored to be in alphabetical order? I noticed the same thing in other places.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/20#discussion_r2426246296" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like that you added `.toLowerCase()` here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/20#discussion_r2426249328" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe these 2 lines could be combined?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/20#discussion_r2426252471" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe add JavaDoc here?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/20#discussion_r2426253961" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe add your name here? Also notice same issue in other places.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/20#discussion_r2426255722" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe update JavaDoc with your exceptions here?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/20#discussion_r2426258654" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like that you used `"delete expense".length()` here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/54#discussion_r2450538254" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice catch
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/61#discussion_r2452418085" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good Explanation
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/89#discussion_r2470277740" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice addition of links
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/89#discussion_r2470279701" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice formatting change to the document
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/96#discussion_r2472158859" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe this should be 2.2.5?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/96#discussion_r2472160848" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice update of User Stories
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/96#discussion_r2472161916" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good Catch!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/102#discussion_r2472915223" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good Addition
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/171#discussion_r2483179222" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe include the `help` command here?
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 19. CHEW.. JEN `@zeeeing` (**16** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/25#discussion_r2429484571" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Don't change this
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/25#discussion_r2429485561" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Revert back to previous version
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/25#discussion_r2429492279" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You forgot to remove this file
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/25#discussion_r2429504132" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Remove this chunk
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/25#discussion_r2429504590" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Remove
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/25#discussion_r2429505335" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Keep line changes minimal
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/28#discussion_r2434342634" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can check here if it is necessary to import junit via mockito?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/28#discussion_r2437889931" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

you havent removed it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/54#discussion_r2454152661" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

what's this for ah? doesn't seem to relate to the current PR description
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/60#discussion_r2464301363" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Possible to rename this to a more descriptive var?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/60#discussion_r2464303157" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think we should keep the declared var unless you have already standardised this across the codebase?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/60#discussion_r2464307762" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I don't think we need this in the scope of our tp
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/60#discussion_r2464308138" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

why you add additional whitespace?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/60#discussion_r2464310833" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

can we remove the 'contact support' hahaha
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/60#discussion_r2464310939" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/60#discussion_r2464312534" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

its a legacy file, don't change it.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/63#discussion_r2468015000" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Sounds good, let me add a table of contents too
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/12#issuecomment-3400888226" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

I have synced my PR to this issue because it's an extension of the deliverables here. Closing this issue now.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/37#issuecomment-3414190353" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

Theres no assertion used in `CreateCommand.java`, can you please check again, thanks
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/59#issuecomment-3454706324" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

See updated issue description for the workload split
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/103#issuecomment-3483249747" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

yeap agree on this, should be labeled as bug
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/134#issuecomment-3483260542" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

PR automatically closed as changes were reflected in PR #138 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 20. CELE.. TAN `@xelisce` (**15** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/18#discussion_r2412646852" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This method is a little long, is there any way to make it more reader-friendly by either abstracting it into functions or adding more comments?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/18#discussion_r2412649907" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could you add a comment / javadoc to explain this?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/27#discussion_r2417228411" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This seems to be specific to the EDIT command and maybe the add command. Could we rename these to something like VALID_CASE_FLAGS so that it reflects that these flags are to be used when adding, accessing or modifying cases?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/27#discussion_r2417231906" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe you could avoid magic strings?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/27#discussion_r2417233032" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you can leave the error messages in here or another class instead of in the Parser (which also has magic strings)?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/37#discussion_r2418342276" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This if else is not needed anymore since the entire thing is wrapped in a try block?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/37#discussion_r2418343277" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you could consider removing the validation logic to Parser or some other class instead of here?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/138#discussion_r2465069931" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should voyeurism be in lower case here?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/132#discussion_r2466767561" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe you could add the "\t" inside your formatLineNoTruncate? to avoid this repetition
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/132#discussion_r2466772724" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps you might want to put a name to this 55 magic number
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/132#discussion_r2466774315" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Remember to change your magic number here too!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/132#discussion_r2466780332" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I believe you can also move the null check into formatLineNoTruncate?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/132#discussion_r2466785032" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I believe you don't need a try catch here, as the mainLoop already try catches. You just have to throw the exception and the mainLoop will print the exception message

```
/**
     * Parses and executes a user command.
     *
     * @param userInput the raw input string entered by the user
     */
    private static void handleUserCommand(String userInput) ``{``
        try ``{``
            Command command = Parser.parseInput(userInput);
            command.execute();
            storage.saveToFile();
        ``}`` catch (InvalidCommandException e) ``{``
            Display.printMessage(e.getErrorMessage());
        ``}``
    ``}`` 
```
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/132#discussion_r2466786397" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Small nitpick: there is a double comment here 
`////`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/157#discussion_r2469323345" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think you meant to change the tip here? Because help doesnt exit the application?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/11#discussion_r2403707169" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

I’ve switched to using a private commandType with a getter in the Command class. Makes things cleaner and keeps it consistent with how we usually handle fields. Appreciate the suggestion!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/11#discussion_r2403707675" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Yep, I’ve extracted the strings into named constants to avoid magic literals. Makes things cleaner and easier to maintain, especially when we reuse some texts for multiple invalid error messages. Thanks for pointing it out!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/9#discussion_r2403708652" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Changed the package for case files to domain.casefiles!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/9#discussion_r2403708722" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed, made this private!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/8#discussion_r2403709142" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks for the feedback, modified the name to handleUserCommand()
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/151#discussion_r2469356083" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Understood, I have created a separate class altogether
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/152#issuecomment-3457104741" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

Need to state that supposed behaviour is to not list down case specific stuff and only the general case details (e.g. murder weapon). Also modify command to direct user to use the read command
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/167#issuecomment-3457520830" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Also for edit command
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 21. TAN ..N YI `@Tanjy55` (**15** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/69#discussion_r2459265316" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM

could consider adding some border format test in next update

eg to check width and ensure border is not jagged/uneven:
assertEquals(expectedWidth, line.length());

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/83#discussion_r2472716897" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

ok this works too 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/83#discussion_r2472724965" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

minor typo "this"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/83#discussion_r2472727808" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

ok to merge as we will update DG again tomorrow
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/88#discussion_r2473370575" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thanks for fixing magic literals
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/88#discussion_r2473375024" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

test looks good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/92#discussion_r2476257285" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good for code quality grading
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/92#discussion_r2476257457" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thanks for adding logging
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/92#discussion_r2476258329" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

wonder if this changes any test condition for junit
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/99#discussion_r2478248522" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice one
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/153#discussion_r2483701386" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

we'll need to update DG/UG for this
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/153#discussion_r2483701724" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

fix looks good also
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/153#discussion_r2483701784" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

logic is correct
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/153#discussion_r2483702483" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good additions for test
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/156#discussion_r2483708881" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

From previous PR, the comment in parse states that add quote is now available in all state
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/47#discussion_r2438410431" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks for the check, removed in later commit.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/56#issuecomment-3417086234" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

failing due to junit test violation :(

@jyx0615 could you advise on what to modify for execute_addQuoteCommand_success
@irw9n could you advise on what to modify for execute_navigateToDifferentQuote_success
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/57#issuecomment-3421945135" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

> Conflicts

resolved
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/64#issuecomment-3430462829" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

Looks good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/136#issuecomment-3475826509" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

Do we switch back to default theme?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/146#issuecomment-3475827191" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

Closed as specific sequence diagram is not mentioned, we are not able to resolve the issue.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/145#issuecomment-3475856768" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

Is this fixable? (im thinking some exception handling + error message)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/144#issuecomment-3475860352" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Interesting.

what happens:
user input “💰” (U+1F4B0)

String s = "\uD83D\uDCB0";  //stored as such
System.out.println(s);
ternimal does not support unicode, and displays ??

Proposed solution:
Since companynames do not contain unicode (typically), modify parser to prevent accepting unicode value
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/142#issuecomment-3475860803" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Needs exception handling in parseExportCommand
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/141#issuecomment-3475861265" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

options:
1) modify error message (e.g. make sure no whitespace)
2) modify parser
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/140#issuecomment-3475861549" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

Set limit to item price, qty, tax rate

Grand total should be less than number of character spacing defined by us (eg 9999999, eg 9.99 million)
-> higher amount can be set as "future update"

This will fix both export PDF and show format issues due to large grand total


reference #134, should we limit number of items also?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/139#issuecomment-3475861828" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

related to #140, closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/138#issuecomment-3475864395" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

options:
1) edit error message (incorrect format or quote does not exist)
2) implement exception handling for nonexistent quote

For first option, we can edit parser:169

'catch (QuotelyException e) ``{``
            logger.warning("Failed to navigate to target with name: " + targetQuoteName);
            throw new QuotelyException(QuotelyException.ErrorType.WRONG_COMMAND_FORMAT,
                    "nav main OR nav n/QUOTE_NAME");
        ``}``'

Modify error message
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/136#issuecomment-3475864733" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

> Would this one be better? [new release](https://github.com/AY2526S1-CS2113-W10-1/tp/releases/tag/new-theme)

Much better

Lets use this theme for v2.1

edit: may need to check if loading is still slow with new theme
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/137#issuecomment-3475865520" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Interesting, thought it would parse nav main first

requires code tracing
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/135#issuecomment-3475865708" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

bundle with #140

closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/134#issuecomment-3475866435" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

bundle with #140 closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/129#issuecomment-3475867212" expanded>
<div slot="header">

**33 :octicon-comment:** %%(other comment)%%
</div>

ideal case: default to quote name (may be hard to implement?)
alt case: print error message (parser should be able to remove whitespace and verify empty field given)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/128#issuecomment-3475867804" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

Can be included as future update: implement selective deletion function

delete i/item p/3 (position 3)

Reason: may not have time to implement
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/126#issuecomment-3475868045" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

parseExportCommand can limit length of name argument
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/125#issuecomment-3475868662" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

I think this is a legitimate issue. 

Propose to have additional Gson file (and corresponding method in storage/jsonserializer) to maintain companyname persistence
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/119#issuecomment-3475869166" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

bundled with #136

closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/123#issuecomment-3475869798" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

I think we should implement:
1) exception handling + error message
2) list this in future update
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/122#issuecomment-3475870155" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

showHelpMessage can be implemented in ui
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/118#issuecomment-3475872107" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

The issue is that user is in main menu state

Calculate total command can be modified to print different error message according to QuotelyState
- in main menu -&gt; "please navigate to quote first"
- in quote "the command format is incorrect..."

similar to #116
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/116#issuecomment-3475888533" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

Modify exception handling

Parser line 222
'catch (QuotelyException e) ``{``
            logger.warning("Failed to find quote for export with name: " + quoteName);
            throw new QuotelyException(QuotelyException.ErrorType.WRONG_COMMAND_FORMAT,
                    "export [n/QUOTE_NAME] [f/FILENAME]");
        ``}``'

should be   'throw new QuotelyException(QuotelyException.ErrorType.QUOTE_NOT_FOUND, ...)';
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/115#issuecomment-3475890518" expanded>
<div slot="header">

**42 :octicon-comment:** %%(other comment)%%
</div>

Remove this portion from parsedeleteitemcommand?

'if (state.isInsideQuote() && quoteName != null) ``{``
                logger.warning("Attempted to use n/QUOTE_NAME while inside a quote");
                throw new QuotelyException(QuotelyException.ErrorType.INVALID_STATE);
            ``}``'
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/114#issuecomment-3475892467" expanded>
<div slot="header">

**43 :octicon-comment:** %%(other comment)%%
</div>

identical to #138, closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/113#issuecomment-3475895338" expanded>
<div slot="header">

**44 :octicon-comment:** %%(other comment)%%
</div>

Wondering why 

`String targetName = arguments.trim();`

does not remove the whitespace
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/112#issuecomment-3475895774" expanded>
<div slot="header">

**45 :octicon-comment:** %%(other comment)%%
</div>

identical to #138 

closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/141#issuecomment-3475896491" expanded>
<div slot="header">

**46 :octicon-comment:** %%(other comment)%%
</div>

Similar issues #113 #111 #110
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/111#issuecomment-3475896728" expanded>
<div slot="header">

**47 :octicon-comment:** %%(other comment)%%
</div>

identical to #141 

closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/110#issuecomment-3475898061" expanded>
<div slot="header">

**48 :octicon-comment:** %%(other comment)%%
</div>

identical to #141 

closed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/109#issuecomment-3475901573" expanded>
<div slot="header">

**49 :octicon-comment:** %%(other comment)%%
</div>

Maybe parser reutrns command for error message when arguments quantity is invalid?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/46#issuecomment-3475952795" expanded>
<div slot="header">

**50 :octicon-comment:** %%(other comment)%%
</div>

Added to `future implementations` in DG / UG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/45#issuecomment-3475952883" expanded>
<div slot="header">

**51 :octicon-comment:** %%(other comment)%%
</div>

Added to `future implementations` in DG / UG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/44#issuecomment-3475953030" expanded>
<div slot="header">

**52 :octicon-comment:** %%(other comment)%%
</div>

Added to `future implementations` in DG / UG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/152#issuecomment-3476110881" expanded>
<div slot="header">

**53 :octicon-comment:** %%(other comment)%%
</div>

should be treated as wrong format and give error message

This is in case user did not mean to delete q1
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/154#issuecomment-3476115191" expanded>
<div slot="header">

**54 :octicon-comment:** %%(other comment)%%
</div>

Tester mentioned that it could use the currently selected quote as the name (get it from QuotelyState)

However I think it will be better to give error message and prompt user for correct command
1) this is in line with how other invalid command behaves
2) this could be a good feature for tester A, but might be intepreted as a bug for tester B (i.e. tester B thinks that saving with invalid input is a bug)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/153#issuecomment-3476343546" expanded>
<div slot="header">

**55 :octicon-comment:** %%(other comment)%%
</div>

Logic looks correct

If can be parsed but exception thrown = quote does not exist
If cannot be parsed (empty string) = invalid command
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/156#issuecomment-3476349988" expanded>
<div slot="header">

**56 :octicon-comment:** %%(other comment)%%
</div>

Looks good, we can test against the list of previously reported bugs after making all code changes, before v2.1 submission 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/109#issuecomment-3476351494" expanded>
<div slot="header">

**57 :octicon-comment:** %%(other comment)%%
</div>

Technically it isnt an error (and i would even consider it a feature, to be able to parse such funny inputs) 

However to user, it may seem like odd behaviour/buggy - especially someone who is purposely looking for bugs

Overall it is a lower priority thing (since program is not crashing) + user will be able to see in the quote that `apple i/book` is keyed in (after which they should know to re-enter the item). 

So we can fix it but last priority
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/136#issuecomment-3476378080" expanded>
<div slot="header">

**58 :octicon-comment:** %%(other comment)%%
</div>

Dinky theme works 

Verified with external tester
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/125#issuecomment-3480196746" expanded>
<div slot="header">

**59 :octicon-comment:** %%(other comment)%%
</div>

Resolved in PR: #162 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 22. RYAN..FONG `@rsiowkf` (**12** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/43#discussion_r2418381283" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Setup is clean and test names follow a descriptive pattern!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/43#discussion_r2418381387" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good test coverage -- covering multiple meals
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/43#discussion_r2418382035" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could we add a test to test for edge cases? such as invalid meals?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/76#discussion_r2446907503" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good use of switch type to handle the different cases! The exception handling was clean and it was easy to read what the code was trying to implement
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/76#discussion_r2446910216" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of assertions to add a layer of defensiveness to the code
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/88#discussion_r2459121054" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of checks and Logger to catch exceptions
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/88#discussion_r2459121513" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good assertions!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/119#discussion_r2472791522" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch of the exceptions. Instead of using a magic number 10000, could we assign a final constant to it instead?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/119#discussion_r2472798573" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could we consider defining a constant to replace "MEAL" in this case?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/119#discussion_r2472802758" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job splitting it up into multiple lines for readability
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/196#discussion_r2484888825" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good job on the use of .filter to ensure that we're capturing the milk pumped today. Overall code is clean and readable.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/196#discussion_r2484889005" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good use of Junit tests to ensure that the code is functioning
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/194#issuecomment-3478006060" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Good use of diagrams to illustrate the classes you've implemented!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/184#issuecomment-3478065943" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

Removed loading sample data.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/167#issuecomment-3481302561" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Jewel solved this issue already
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/187#issuecomment-3481339067" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

To keep all the different goals created in the list. Latest input for goal will be updated as the current workout goal 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/216#issuecomment-3483685222" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

Good use of logger levels to show severity of issues
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 23. SHAU.. REN `@shauntsr` (**12** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/45#discussion_r2431671357" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could consider changing to follow our current naming convention. Can refer to the other tests written.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/49#discussion_r2435497215" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could this be in parser instead?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/49#discussion_r2435507556" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would this cause double printing of message?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/49#discussion_r2435512213" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Inconsistent naming convention compared to ZettelTest
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/86#discussion_r2464916938" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe could prefix with which object is self-linking e.g. NoteSelfLinkException

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/86#discussion_r2464936415" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Potentially confusing naming, I was unable to figure out where the outgoing link is from
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/87#discussion_r2467743519" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could consider breaking into 2 if statements instead of if, else-if since throw immediately returns
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/87#discussion_r2467762353" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could consider joining both branches with a OR since the actions are the same
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/90#discussion_r2469043959" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could consider changing isLinkedTo to the outgoings notation
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/106#discussion_r2476156581" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should deletion of tag globally also delete it from tags.txt?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/109#discussion_r2477054556" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Might be better to throw exception?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/109#discussion_r2477069829" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could consider abstracting into Storage/FileSystemManager, seems abit out of place here.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/189#issuecomment-3475999128" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Closing as no specific bug
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/185#issuecomment-3476021123" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

Closed as it is error is correctly specified
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/181#issuecomment-3476032469" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #184 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/175#issuecomment-3476041897" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

Add a line break
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/174#issuecomment-3476043131" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

Change DG comment
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/171#issuecomment-3476046173" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

Rename variable
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/156#issuecomment-3476061858" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

Validate note title length 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/176#issuecomment-3476429349" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

Done

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/173#issuecomment-3476436572" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

Closing since it is part of puml design
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/172#issuecomment-3476438517" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

Done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/170#issuecomment-3476439355" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/169#issuecomment-3476450540" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Done

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/167#issuecomment-3476451686" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

Done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/165#issuecomment-3476452843" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

Done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/163#issuecomment-3476453776" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

Done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/135#issuecomment-3476477365" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

Cannot find the issue.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/132#issuecomment-3476480696" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

Done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/209#issuecomment-3477759418" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Sub-issues resolved
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/183#issuecomment-3478054197" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

Issues are separate; time out is due to not inputting any commands within the past 3 minutes. However, will still address the duplicate repo message.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 24. GADD..IRAM `@argadde` (**12** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432456683" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Simply for code style, consider capitalizing the logger to "LOGGER" for the variable name. Also, is there a reason you included the logger.setLevel? Maybe you could consider just stating the logger level depending on the message and use case throughout the code.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432462923" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I like this type of format but looks like the course website prefers this format: "// log a message at INFO level
logger.log(Level.INFO, "going to start processing");"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432464139" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same as above for all logging.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432507062" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Oh okay, perfect I'll set add-pet to do the same. I didn't realize INFOs still show up at runtime.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/46#discussion_r2432509402" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Yeah, I'm honestly unsure, but that's the example format given on the topics of this week, so it might just be a safe bet.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/43#discussion_r2432526376" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Since this is a final static, you could consider capitalizing the variable to "LOGGER". Also, you could add a brief code snippet under to ensure any INFOs don't show up in runtime:

static ``{``
        LOGGER.setLevel(Level.WARNING);
    ``}``
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/43#discussion_r2432527838" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great use of logging! This is the perfect format, according to style guidelines.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/43#discussion_r2432530206" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You could consider adding a log here as well.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/43#discussion_r2432534514" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

In add-treatment, you use level INFO while here you use level FINE for executing the command. Maybe you could choose one (INFO, in this case)?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/117#discussion_r2472335973" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You could consider lowercasing "interface" since that's how it's written in the examples.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/117#discussion_r2478200346" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

If command fails, should it not stop the execution? Wasn't it correct beforehand?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/124#discussion_r2478279928" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Don't think this is too big of a problem. This current implementation will look cleaner when called within the codebase.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/20#discussion_r2405205371" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ya I'm not quite sure. the User Guide that we wrote up had it as "add pet" so I had to change the parsing logic
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/20#discussion_r2405205998" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

alternative would be maybe "add-pet"?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/50#discussion_r2432557853" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Okay, that's fair. Initially, I wanted the logs to contain everything but I can see how the user could end up seeing the message twice since i'm already printing error message.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/94#discussion_r2452644866" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

I dont think so. "--o" states that AddPetCommand has/uses PetList.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/122#issuecomment-3460834308" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>


<img width="340" height="88" alt="Screenshot 2025-10-29 at 8 05 57 PM" src="https://github.com/user-attachments/assets/719655ee-cc73-42f2-becf-c51aad331314" />


This is how the save file looks like.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 25. GOH .. ANH `@JeanPerrierIII` (**11** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/84#discussion_r2462741450" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good description
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/97#discussion_r2466449686" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Well done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/99#discussion_r2468146973" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

looks good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/176#discussion_r2483739636" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

looking good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/176#discussion_r2483739696" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

put HH:mm, Number of tasks(n) in square brackets as it is optional flag, see ##Features at the top of the file
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/180#discussion_r2484384834" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good changes
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/181#discussion_r2484386365" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good changes
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/181#discussion_r2484387405" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

looks good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/190#discussion_r2486725477" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

All ok
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/195#discussion_r2487128468" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

No issues found; looks good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/208#discussion_r2487854893" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good changes, very detailed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/11#issuecomment-3368224306" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Implemented in [9e7a314](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/9e7a314015e62cc264766777735bc7b8ce042ea4)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/9#issuecomment-3368224383" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Implemented in [9e7a314](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/9e7a314015e62cc264766777735bc7b8ce042ea4)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/7#issuecomment-3368225660" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

Implemented in [a63bc3c
](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/a63bc3c9320e9846ea45212848490e7f9161af1b)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/35#issuecomment-3388289071" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Complete in comit [f15012a](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/f15012abd87fd8d4acdbf3de1a7b9044159ac8c0)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/41#issuecomment-3389081041" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [8496fd8](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/8496fd8530645c9f3060c72825d6d6001c17df33)

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/34#issuecomment-3403145536" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

Fixed in commit [672ec46](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/672ec46f4e50e1f7168962dd61a5cfb5f60616bc)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/56#issuecomment-3404420717" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

Superseded by PR [#57](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/57)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/65#issuecomment-3424566224" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

Completed in commit [02030e9](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/02030e9e278de1c024d0b1eee1b332bc0458d5a9)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/123#issuecomment-3475908043" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

To update the UG to specifically mention that the index for the changedeadline command is of index of the task in the list command, not priority of task
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/120#issuecomment-3475908803" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

duplicate of [#118](https://github.com/AY2526S1-CS2113-W12-1/tp/issues/118)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/127#issuecomment-3475920080" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

either indicate in UG/DG that checkcurrent only shows deadlines after the current day's date or implement feature to tell user that they have overdue tasks
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/126#issuecomment-3475928391" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Indiciate in UG/DG that the first number in the changepriority corresponds to items index rather than priority of task
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/124#issuecomment-3475933992" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Dupllicate of [#126](https://github.com/AY2526S1-CS2113-W12-1/tp/issues/126)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/131#issuecomment-3476050261" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #127
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/133#issuecomment-3476060203" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #130
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/118#issuecomment-3476336269" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

Fixed in commit #[21f1644](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/21f1644a8e006ef7b174618268db75577d5332b6)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/119#issuecomment-3476336467" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

Fixed in [21f1644](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/21f1644a8e006ef7b174618268db75577d5332b6)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/121#issuecomment-3476336664" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [dfe2c20](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/dfe2c20ee8d124c1c03f3e6b742cc39bcb4972d9)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/122#issuecomment-3476336866" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [4fae02c](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/4fae02c944e9ce450d557e9c00fcc00c72692e52)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/123#issuecomment-3476336953" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [6dfe0ad](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/6dfe0adf2672f873477294b547fafc81c20cb881)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/125#issuecomment-3476337232" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [e716bfa](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/e716bfaf5dee502e2480fb8e159ac70822172a05)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/126#issuecomment-3476337389" expanded>
<div slot="header">

**33 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [356b19c](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/356b19c643c7ab8aca98617d81ae9efe05beb850)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/127#issuecomment-3476337828" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [3844fa3](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/3844fa31b246167d9632072ccf5a3e610be75f66)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/128#issuecomment-3476338113" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [e716bfa](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174/commits/e716bfaf5dee502e2480fb8e159ac70822172a05)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/156#issuecomment-3476342924" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #119 

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/137#issuecomment-3476347791" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #118
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/138#issuecomment-3476348441" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #122
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/154#issuecomment-3476351447" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #130
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/168#issuecomment-3476353425" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #126 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/172#issuecomment-3476382944" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #146
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/171#issuecomment-3476383063" expanded>
<div slot="header">

**42 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #142
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/163#issuecomment-3476383527" expanded>
<div slot="header">

**43 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #140
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/157#issuecomment-3476385018" expanded>
<div slot="header">

**44 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #119
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/151#issuecomment-3476386508" expanded>
<div slot="header">

**45 :octicon-comment:** %%(other comment)%%
</div>

Do we have another commany summary elsewhere
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/136#issuecomment-3476401040" expanded>
<div slot="header">

**46 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [6bb9fcf](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/175/commits/6bb9fcf578f39e03a32e7234de1f68032b42132a)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/149#issuecomment-3476401235" expanded>
<div slot="header">

**47 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [67316f6](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/175/commits/67316f602217b44980bbcead3a3d3885b941f714)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/140#issuecomment-3476401414" expanded>
<div slot="header">

**48 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [26a3bb6](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/175/commits/26a3bb6fa29341597218641be25c4b15fbf11e64)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/147#issuecomment-3476401704" expanded>
<div slot="header">

**49 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [e673f01](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/175/commits/e673f012900aad57d414cedbbab71e98c948b589)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/145#issuecomment-3476401899" expanded>
<div slot="header">

**50 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [6ac3a67](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/175/commits/6ac3a6702fdc5e37171629d4dbf026f302fd31d9)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/142#issuecomment-3476402135" expanded>
<div slot="header">

**51 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [919faab](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/175/commits/919faab4b86db8d32afce4b49665ef04e31d0d47)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/146#issuecomment-3476402445" expanded>
<div slot="header">

**52 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [b724bd1](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/175/commits/b724bd1023a33ea978cf6b300adf6cd1aac81a1c)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/150#issuecomment-3476451683" expanded>
<div slot="header">

**53 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [ba113ad](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/177/commits/ba113ad11479e36b3d5f4224e63e7f6ee8f72af8)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/160#issuecomment-3479246675" expanded>
<div slot="header">

**54 :octicon-comment:** %%(other comment)%%
</div>

Duplicate of #135 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/166#issuecomment-3479256574" expanded>
<div slot="header">

**55 :octicon-comment:** %%(other comment)%%
</div>

Resolved in PR #182 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/164#issuecomment-3479267858" expanded>
<div slot="header">

**56 :octicon-comment:** %%(other comment)%%
</div>

Resolved in commit 
[65a6a6a](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/65a6a6ac1a4c320d76f730376713c9c9cf30b540)

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/135#issuecomment-3480159551" expanded>
<div slot="header">

**57 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [8eefb9c](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/185/commits/8eefb9cafc578df2c77760016f85042035c3f329)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/162#issuecomment-3480160539" expanded>
<div slot="header">

**58 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [8eefb9c](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/185/commits/8eefb9cafc578df2c77760016f85042035c3f329)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/132#issuecomment-3480347112" expanded>
<div slot="header">

**59 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [4df93b7](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/185/commits/4df93b7c6e9ad99cb060e68a2420819f61079081)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/151#issuecomment-3481175727" expanded>
<div slot="header">

**60 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [b2ddaf5](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/190/commits/b2ddaf583f909c3df8b04fefe7ed02da259f7cde)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/169#issuecomment-3481177755" expanded>
<div slot="header">

**61 :octicon-comment:** %%(other comment)%%
</div>

Resolved in [3214021](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/190/commits/32140213fbd38b1df2e24a8465ccc1f9c9660a89)
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 26. DANI.. WEI `@danielkwan2004` (**11** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/109#discussion_r2476910468" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

please keep consistent format. "Archive notes format should be: ..."
this is consistent with the rest of the FORMATs above.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/109#discussion_r2476922288" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Gordon this is wrong. now list linked notes command have their own format, which is list-outgoing-links &lt;note_ID> and list-incoming-links &lt;note_ID>. it no longer needs to be parsed into parselistnotecommand before being routed to parselistlinkednotescommand
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/109#discussion_r2476937290" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Confirm that notes.size() is the count of the notes for that specific type ? (either all pinned, all archived, or both pinned and archived, or all). Just clarifying if you have checked this
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/115#discussion_r2478197194" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

showRepoSuccessfullyChanged
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/115#discussion_r2478203031" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

showCurrentRepoSuccesfully
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/211#discussion_r2483779173" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

this is wrong we were called out for this during PE it supposed to take list [-p] [-a] where -p and -a can be in any order
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/216#discussion_r2484437808" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

refer to the truth table below to change the language. 
list -p: pinned == 1, archived == 0
list -p -a: pinned == 1, archived == 1
list -a: pinned == X, archived == 1
list: pinned == X, archived == 0

where X means both pinned and unpinned will be shown.
there will NEVER be a case where both archive and unarchive are shown.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/216#discussion_r2484440338" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

i don't see this being used anywhere in this file
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/216#discussion_r2484442472" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should it be change-repo[sitory]? just a question
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/216#discussion_r2484443227" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

same comment below for change-repo[sitory]
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/216#discussion_r2484446175" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

missing space between the + and the const string
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/49#discussion_r2435847983" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

fixed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/49#discussion_r2435850914" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

fixed. it was double printed originally as well
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/87#discussion_r2468352374" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/87#discussion_r2468354307" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

good catch
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/86#issuecomment-3452622693" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

@new reviewer, please re-review the changes. now all the validation of the noteIds take place in the parser level. all commands that require the use of noteIDs assume that the noteIds being passed into the commands are already validated. I also renamed the linking naming conventions to be clearer as specified by @shauntsr who reviewed previously. now, say we want to link A -&gt; B. the naming convention of A would be sourceNote and B is the targetNote. 

each of these notes will store:
1. an outgoingLinks hashmap, that is a collection of notes that the current note is pointing to.
2. an incomingLinks hashmap, that is a collection of notes that is pointing to the current note.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/202#issuecomment-3475996982" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

@JianHao24 simple fix 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/201#issuecomment-3476002397" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

@shauntsr remove the logger info it is cluttering up what the user sees. we already put in the UG that if a tag doesn't exist and a note is tagged with that new tag, it will both tag the note and auto create a new tag. check if this logic is consistent.

Don't touch the UG

maybe check if the DG is consistent
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/200#issuecomment-3476005535" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

should be simple fix @gordonajajar 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/198#issuecomment-3476008072" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

@gordonajajar fix DG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/184#issuecomment-3476027187" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

Change the spelling of the log message, ban any non alphanumeric characters and symbols.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/182#issuecomment-3476030367" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

Add to UG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/180#issuecomment-3476033270" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

we are not doing this. init will create but not change
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/179#issuecomment-3476035349" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Tell the user on startup that there is no repo created and will default to main
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/177#issuecomment-3476039282" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

Add a line of lines, in the main loop instead of UI.java.

Modify Zetteltest.java if needed.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/175#issuecomment-3476042040" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

Add a linebreak because when converted to PDF it will screw up
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/168#issuecomment-3476049139" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

special character duplicate
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/166#issuecomment-3476050554" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

the first part is a duplicate, so only look at the second part.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/161#issuecomment-3476057882" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

first part is duplicate, only look at the &lt;&lt;class>> parser
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/154#issuecomment-3476063759" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

duplicate
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/153#issuecomment-3476064287" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

indentation error
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/152#issuecomment-3476067908" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

change find to allow searching for the body using multiple spaced strings.

also create a new find function to find based on the title and print out the note's title and hash
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/149#issuecomment-3476069693" expanded>
<div slot="header">

**33 :octicon-comment:** %%(other comment)%%
</div>

Indentation issue
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/138#issuecomment-3476075462" expanded>
<div slot="header">

**34 :octicon-comment:** %%(other comment)%%
</div>

Please change the help message to update accordingly with the new commands and the new formats.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/138#issuecomment-3476078290" expanded>
<div slot="header">

**35 :octicon-comment:** %%(other comment)%%
</div>

Change parser FORMAT
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/137#issuecomment-3476079161" expanded>
<div slot="header">

**36 :octicon-comment:** %%(other comment)%%
</div>

Update UG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/133#issuecomment-3476083670" expanded>
<div slot="header">

**37 :octicon-comment:** %%(other comment)%%
</div>

Duplicate scroll bar in pdf
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/195#issuecomment-3476092596" expanded>
<div slot="header">

**38 :octicon-comment:** %%(other comment)%%
</div>

Replace all spaces with underscores, define this in the UG.

Must use in conjunction with banning special characters in the title.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/150#issuecomment-3476098075" expanded>
<div slot="header">

**39 :octicon-comment:** %%(other comment)%%
</div>

specify in user guide that emojis are not allowed, and if you want emojis you have to check if your note editor/terminal can support it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/148#issuecomment-3476098961" expanded>
<div slot="header">

**40 :octicon-comment:** %%(other comment)%%
</div>

Change UG and remove logging message
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/147#issuecomment-3476100272" expanded>
<div slot="header">

**41 :octicon-comment:** %%(other comment)%%
</div>

standardize to american english
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/144#issuecomment-3476101322" expanded>
<div slot="header">

**42 :octicon-comment:** %%(other comment)%%
</div>

No. that's your problem.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 27. JIAN..XUAN `@jyx0615` (**11** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/25#discussion_r2400667413" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

How about passing the entire `state` to the parser and removing `state` from command execution?

If we want to support adding an item with a quote name outside a quote, as well as adding an item inside a quote without specifying the quote name, moving `state` into the parser would help. The parser can handle extracting the quote from either the `state` or the user command and then pass it to the command, so the command interface remains consistent in both cases.

What do you think?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/25#discussion_r2400670485" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

If we decide to move the `state` to the parser, I can do the exception handling for that inside parser.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/34#discussion_r2430973203" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

How about changing it into two condition: navigating to the same quote and all other scenario. Alternatively, we could simply display the same message for all initial conditions and can further remove if and else statement.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/47#discussion_r2438004380" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should we remove this line?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/55#discussion_r2441527876" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

How about using `logger.severe(e.getMessage())` to keep it consistent with the other log formats?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/56#discussion_r2441534539" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

- AddQuoteCommandTest > execute_addQuoteCommand_success() FAILED

Consider adding `state.setOutsideQuote();` in the test method, since I changed the `QuotelyState` class to a singleton and may retain state from previous tests.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/56#discussion_r2441534677" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

- NavigateCommandTest > execute_navigateToDifferentQuote_success() failed.

Since the user may start from the main menu and navigate to another quote, this assertion could fail in that case. It might be better to remove this assertion.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/64#discussion_r2450168483" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Line 49 already enables the assertion — consider keeping just one for clarity.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/80#discussion_r2471610646" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Do we need to get an approval to use this library?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/78#discussion_r2471617757" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Just to confirm — is this file path compatible with all operating systems? Some systems may handle path separators differently. Consider using [file path in os independent way](https://www.sghill.net/2014/how-do-i-make-cross-platform-file-paths-in-java/).

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/90#discussion_r2476115173" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice work — converting to lowercase before comparison makes the logic more robust.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/2#discussion_r2368766517" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

a4aaa29
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/2#discussion_r2368767658" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

a4aaa29
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/2#discussion_r2368768412" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

a4aaa29
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/27#discussion_r2401029021" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

efd135d
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/27#discussion_r2401029301" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

efd135d
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/27#discussion_r2401029591" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

efd135d
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/27#discussion_r2401029819" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

efd135d
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/28#discussion_r2406666089" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

2c4cfe5
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/29#discussion_r2419367424" expanded>
<div slot="header">

**20 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

2f51179
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/29#discussion_r2419367762" expanded>
<div slot="header">

**21 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

2f51179
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/31#discussion_r2422496221" expanded>
<div slot="header">

**22 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

1ed2ffe
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/31#discussion_r2422496229" expanded>
<div slot="header">

**23 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

1ed2ffe
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/32#discussion_r2422507272" expanded>
<div slot="header">

**24 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

46fe0f0
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/32#discussion_r2422507286" expanded>
<div slot="header">

**25 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

46fe0f0
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/32#discussion_r2422507298" expanded>
<div slot="header">

**26 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

46fe0f0
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/51#discussion_r2438719818" expanded>
<div slot="header">

**27 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

9286db9
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/60#discussion_r2446629226" expanded>
<div slot="header">

**28 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

52d8e55
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/70#discussion_r2460827116" expanded>
<div slot="header">

**29 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

This is just a sample code. The mock data will be replaced soon.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/73#discussion_r2462243188" expanded>
<div slot="header">

**30 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

e9f3186
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/73#discussion_r2462243209" expanded>
<div slot="header">

**31 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

e9f3186
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/81#discussion_r2471678964" expanded>
<div slot="header">

**32 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ae57dd3
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/81#discussion_r2471679008" expanded>
<div slot="header">

**33 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ae57dd3
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/81#discussion_r2471679050" expanded>
<div slot="header">

**34 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ae57dd3
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/81#discussion_r2471679100" expanded>
<div slot="header">

**35 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ae57dd3
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/81#discussion_r2471679165" expanded>
<div slot="header">

**36 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ae57dd3
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/81#discussion_r2471679238" expanded>
<div slot="header">

**37 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ae57dd3
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/81#discussion_r2471679298" expanded>
<div slot="header">

**38 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ae57dd3
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/88#discussion_r2473359947" expanded>
<div slot="header">

**39 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

79f9cc0
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/92#discussion_r2476156171" expanded>
<div slot="header">

**40 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

4729795
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/92#discussion_r2476201580" expanded>
<div slot="header">

**41 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

c22f922
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/94#discussion_r2476657834" expanded>
<div slot="header">

**42 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

9d30f95
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/94#discussion_r2476657943" expanded>
<div slot="header">

**43 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

9d30f95
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/94#discussion_r2476658074" expanded>
<div slot="header">

**44 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

9d30f95
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/156#discussion_r2483551083" expanded>
<div slot="header">

**45 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

4e6ddae
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/156#discussion_r2483551507" expanded>
<div slot="header">

**46 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

4e6ddae
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/157#discussion_r2483765899" expanded>
<div slot="header">

**47 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

2640cf0
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/157#discussion_r2483765942" expanded>
<div slot="header">

**48 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

85e5d7f
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/158#discussion_r2484160531" expanded>
<div slot="header">

**49 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

137735c
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/158#discussion_r2484160566" expanded>
<div slot="header">

**50 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

137735c
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/158#discussion_r2484160579" expanded>
<div slot="header">

**51 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

137735c
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/158#discussion_r2484160585" expanded>
<div slot="header">

**52 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

137735c
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/158#discussion_r2484160601" expanded>
<div slot="header">

**53 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

137735c
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/4#issuecomment-3324533495" expanded>
<div slot="header">

**54 :octicon-comment:** %%(other comment)%%
</div>

run `./gradlew checkstyleMain` before commit to check the style
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/4#issuecomment-3327006294" expanded>
<div slot="header">

**55 :octicon-comment:** %%(other comment)%%
</div>

solve the conflicts
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/4#issuecomment-3327057459" expanded>
<div slot="header">

**56 :octicon-comment:** %%(other comment)%%
</div>

Nice job!!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/4#issuecomment-3327058260" expanded>
<div slot="header">

**57 :octicon-comment:** %%(other comment)%%
</div>

Merge into master
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/47#issuecomment-3413472650" expanded>
<div slot="header">

**58 :octicon-comment:** %%(other comment)%%
</div>

Checkstyle rule violations were found.
run `./gradlew checkstyleTest` to check the style of tests.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/52#issuecomment-3414304883" expanded>
<div slot="header">

**59 :octicon-comment:** %%(other comment)%%
</div>

I found that you have no pr labelled with v1.0 so i change this one to v1.0 hope that it will help you get the point of `v1.0 PRs` task in tp dashboard.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/57#issuecomment-3421894769" expanded>
<div slot="header">

**60 :octicon-comment:** %%(other comment)%%
</div>

Conflicts
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/59#issuecomment-3424547500" expanded>
<div slot="header">

**61 :octicon-comment:** %%(other comment)%%
</div>

Looks clean overall!
Just a question — where should we store the tax rate? Should it be inside the `state`, and can it be modified by the user?

Also, there’s a conflict in `AddQuoteCommand.java`.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/100#issuecomment-3468211020" expanded>
<div slot="header">

**62 :octicon-comment:** %%(other comment)%%
</div>

Conflict!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/136#issuecomment-3475856954" expanded>
<div slot="header">

**63 :octicon-comment:** %%(other comment)%%
</div>

Would this one be better?
[new release](https://github.com/AY2526S1-CS2113-W10-1/tp/releases/tag/new-theme)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/119#issuecomment-3475857432" expanded>
<div slot="header">

**64 :octicon-comment:** %%(other comment)%%
</div>

Would this one be better?
[new release](https://github.com/AY2526S1-CS2113-W10-1/tp/releases/tag/new-theme)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/147#issuecomment-3475858708" expanded>
<div slot="header">

**65 :octicon-comment:** %%(other comment)%%
</div>

I also fix it in my pr, so I close the pr. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/141#issuecomment-3475863340" expanded>
<div slot="header">

**66 :octicon-comment:** %%(other comment)%%
</div>

Prefer 2!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/issues/109#issuecomment-3476043360" expanded>
<div slot="header">

**67 :octicon-comment:** %%(other comment)%%
</div>

It treats the item name as `apple i/book` and price = 20, quantity = 5. 
I am not sure whether it should be an error?
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 28. HE P.. SAN `@Kennahh` (**11** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/51#discussion_r2429313640" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

A helpful feature to help users get used to the product.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/51#discussion_r2429316045" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This offers clear input format for the users.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/51#discussion_r2429332082" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The format is not aligned with the example input.  And the example output is not aligned with the example input.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/51#discussion_r2429341482" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can tell the user that the index can be referred from the 'list' command.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/51#discussion_r2429352087" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Need to add 'place' input.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/51#discussion_r2429353989" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Example of adding an exam needs to be updated. (add a place)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/51#discussion_r2429358017" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can add some examples to avoid confusion.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/74#discussion_r2443750141" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can change to:
for (Activity activity: activities) ``{``
    if (activity instanceof Task) ``{``
        ....
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/74#discussion_r2443754780" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

is it better to add the condition of daysBetween >= 0 ?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/190#discussion_r2486732440" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

clear instructions
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/190#discussion_r2486735324" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

will it be clearer to replace "output" to "outcome" since these are not the actual outputs
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/19#issuecomment-3372879728" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Completed in commit d393717e9500d5d7cbaf38d75d5fa11a57b448f5.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/20#issuecomment-3372883479" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Completed in commit b5b19b073cb806c585f86168babd98483b97a95d.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/21#issuecomment-3388360615" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

Implement in 471631f50eadbbf437f7d4416df3029c2064c278
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/76#issuecomment-3422577921" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Looks good. No error found.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/67#issuecomment-3422736766" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

Completed in 66f24d0049dad541dcea07e5e2dc850bf81ff7ed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/94#issuecomment-3451422630" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

Looks good.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/192#issuecomment-3481286458" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 29. MROZ..TRYK `@patrykmrozek` (**11** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/23#discussion_r2453036159" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Why delete all of the JavaDoc comments?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/154#discussion_r2483148517" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I suggest using COMMAND_INSERT.length() or creating another variable instead of using magic number 7
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/154#discussion_r2483148635" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same here as above, COMMAND_DELETE.length() or something else rather than magic number 6
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/158#discussion_r2483833321" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I suggest you store these parts/prefixes in variables like for example PREFIX_COURSE = "c/".
This helps remove magic strings.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/158#discussion_r2483834571" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

In relation to my previous comment, you could also remove these magic numbers by using, for example, PREFIX_COURSE.length() or something similar
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/164#discussion_r2484178489" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

import * will get flagged by checkstyle, import each package individually
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/168#discussion_r2484899460" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

why remove comments
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/168#discussion_r2484899556" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

why removing javadoc comments?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/169#discussion_r2484910464" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

can remove these comments
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/169#discussion_r2484910799" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

can keep comments
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/169#discussion_r2484910944" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

can keep comments here too
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/162#issuecomment-3477380843" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

I feel like the list command could stay but maybe change its functionality to list the module codes only instead of full timetable info as to differentiate it from `show timetable`.
eg:
`list`
```
Here are your modules:
CS0001
CS0002
CS0003
```
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 30. BENJ..KIET `@BenyAlbatross` (**10** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/82#discussion_r2451837980" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider including the original exception inside the log message to help with better debugging. For example,
`logger.severe("Error executing Add Command", e)`
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/82#discussion_r2451844885" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider removing magic numbers for clarity
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/82#discussion_r2451855856" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider making the constants private (private static final), as they are internal magic numbers
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/86#discussion_r2456992118" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

For style consistency purposes, we might want to consider if Company and Role should start with small letters instead.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/86#discussion_r2457009790" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

While this is purely stylistic, you could consider listing the found internships with columns that are equally wide for each row just like in the list command, so that it would be easier for the user to read. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/86#discussion_r2457022317" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The ByteArrayOutputStream is created once and reused across tests. This makes test outputs accumulate across `@Test` methods and could result in some errors. It might be better to create a new ByteArrayOutputStream for each test in `@BeforeEach`.

This is an example from InternshipListTest.java:
```
@BeforeEach
    void setUp() ``{``
        outContent = new ByteArrayOutputStream();
        System.setOut(new PrintStream(outContent));
        InternshipList.clear();
    ``}``
```
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/112#discussion_r2477456743" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Ui should be labelled as «class» for the sequence diagram, as it is calling a static method in Ui. For reference, the ones needing to be labelled as class are Ui, DashboardUi, ArgumentParser, InternshipList.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/198#discussion_r2486745361" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Tiny nit, space needed between else and ``{``
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/198#discussion_r2486799954" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You could consider having findNearestDeadlineInternship return a Java Pair&lt;Internship, Integer>, instead of using the pay field to store count of nearest deadlines
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/198#discussion_r2486807509" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Tiny nit, space needed between else and ``{``
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/62#discussion_r2438637292" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Fixed in latest commit
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/62#discussion_r2438637780" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Fixed in latest commit 👍 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/190#discussion_r2484795549" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Changed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/1#issuecomment-3332149008" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/65#issuecomment-3419531526" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

@lukeai-tan I've been trying to expose the DateFormatter error to the user if a storage file is loaded with the wrong date, but I think that there's an unreachable code.

The regex at line 55 checks for `\d``{``2``}``-\d``{``2``}``-\d``{``4``}```, which means that 
```
catch (NumberFormatException e) ``{``
            throw new InternityException("Date must contain only numbers (expected dd-MM-yyyy)");
        ``}``
```
will never be reached. So I'm unable to create a test case to induce this behaviour.

So just to clarify, currently there are 3 errors that DateFormatter can throw:
1) `InternityException.invalidDateFormat();`
2) 
```
if (!isValidDate(day, month, year)) ``{``
                throw new InternityException("Invalid date: " + trimmed);
            ``}``
```
3) 
```
catch (NumberFormatException e) ``{``
            throw new InternityException("Date must contain only numbers (expected dd-MM-yyyy)");
        ``}``
```
Alternatively on my end, I could treat any date error as a generic error.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 31. LKE..NAIR `@Rezelix` (**10** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/12#discussion_r2396460837" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

bro can u update this john doe to be your name
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/27#discussion_r2434635725" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Diverse set of test cases for automated testing! Good job!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/27#discussion_r2434643212" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good idea for making the output date be in uppercase! This makes it easier for the team to standardize date formats! If for example, there are implementations of date formats that do not make use of the DateTimeFormatter library
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/27#discussion_r2434644321" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good spot of whitespace!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/34#discussion_r2443463538" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good set of JUnit test cases for the data manager! It addresses multiple possible errors that could occur!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/68#discussion_r2458690467" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM, please note that we may need changes later with the numbering of our points!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/68#discussion_r2458714412" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I understand the use of the PlantUML plugin to make the class diagram. While it doesn't adhere to the format shared in lectures, I will approve this first, as there is uncertainty if this is acceptable or not.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/79#discussion_r2465785254" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could be changed to reference frame
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/90#discussion_r2471444442" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could just use * instead of 0..*
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/173#discussion_r2483802288" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good catch
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/36#issuecomment-3422469837" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Resolves #35 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/issues/64#issuecomment-3435474235" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Make UML Diagrams for add, delete and listing investments
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 32. VU D..KHOI `@Exceptional-Khoi` (**10** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/52#discussion_r2426794867" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

These lines repeat 2 times. If you do more of them in the future, consider create a method to implement them!!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/66#discussion_r2428484726" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider adding a negative test case. For example, a record with an unexpected date format or a null date (if WeightRecord allows it). This helps confirm that toString() or getters behave safely with edge inputs.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/68#discussion_r2428607270" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Edge case idea: Add a test for when multiple weight records share the same date or when the history is very long (e.g., verifying getLatestWeight() still works).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/89#discussion_r2438604514" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/89#discussion_r2438604742" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/97#discussion_r2443007040" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice OOP
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/138#discussion_r2457070453" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/140#discussion_r2458767214" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/141#discussion_r2458936024" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

necessary
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/144#discussion_r2459076597" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 33. RYAN.. HAO `@ry-koh` (**8** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/17#discussion_r2422528137" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should be rawDateTime
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422536206" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The name of the reminder
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422536311" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Change to reminder
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422536713" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

does not follow naming convention
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422553778" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

i think it is not very clear what isReminder is for
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422554166" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

commenting structure is wrong should be

@param name *purpose of name*
@param dateTime *purpose pf dateTime*
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422554348" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

would be good to add Javadoc comments here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/21#discussion_r2422555209" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Why is this [O] unlike the previous [X] in deadline and todo
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/20#discussion_r2422037424" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

ok
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 34. LIM ..ERUI `@limzerui` (**8** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/54#discussion_r2423351398" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good test coverage. You could also add one more test for inputs with extra spaces or different letter cases to confirm it works
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/54#discussion_r2423351593" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Might be better to separate usage help from the actual error message so users only see the guide when they really need it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/54#discussion_r2423352016" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This warning is helpful. Could also suggest to the user what the valid range is to make it clearer.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/71#discussion_r2438728611" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

well done on the documentation!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/71#discussion_r2438730519" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

appreciate the formatting
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/96#discussion_r2451738853" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Very meticulous!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/239#discussion_r2483163146" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

this will definitely prevent the edge case. appreciate the change. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/266#discussion_r2487410711" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

definitely adds clearer understanding for readers
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/15#issuecomment-3358885500" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/48#issuecomment-3384587084" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/51#issuecomment-3393373202" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Appreciate the comments @muadzyamani !
Added Javadoc and normalised the double initialisers—please take another look.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/54#issuecomment-3393963041" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Solid hardening of handleDelete.
Extracting parseDeleteCommand() definitely improves separation of concerns and testability. The custom DeleteCommandException also clarifies error paths.

It would be great to make the delete command more forgiving for example, allowing extra spaces or different capitalizations like " delete   3" or "DELETE 3". 
Also, consider separating help messages from actual error messages so that users don’t see the usage format every time something goes wrong (like when they enter an out-of-range index).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/76#issuecomment-3417836220" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/93#issuecomment-3426860346" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/96#issuecomment-3431867962" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Detailed and comprehensive documentation for the edit feature!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/125#issuecomment-3441367834" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

resolve #126 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/112#issuecomment-3441541540" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/130#issuecomment-3445869062" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

detailed sequence diagram. LGTM. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/146#issuecomment-3450574834" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/152#issuecomment-3451867084" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

nice! best to follow best practises :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/165#issuecomment-3457286045" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/178#issuecomment-3461870942" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

appreciate the simpler diagram. it's easier to follow now. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/245#issuecomment-3476179394" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/248#issuecomment-3477969440" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/251#issuecomment-3477990795" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

updated code snippets helps maintaining the feature for future developers. LGTM.

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/253#issuecomment-3477991968" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

 lgtm.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 35. GOH .. WEE `@gbinw128` (**8** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/23#discussion_r2429508595" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Mayb specify what the input is specifically by using @params?

Multiple cases of this spotted
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/88#discussion_r2471735227" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This should be kept.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/88#discussion_r2471735560" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This should be kept.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/88#discussion_r2471738468" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The "br" was added as a personal choice, you can decide whether to keep it. Applies to all the rest
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/88#discussion_r2471739420" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This should be kept.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/111#discussion_r2476312353" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice addition.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/183#discussion_r2486495376" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice catch
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/183#discussion_r2486496206" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good addition!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/issues/122#issuecomment-3475844012" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Edit error message instead of UG
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 36. LUO ..GXUN `@BestBearrr` (**8** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/75#discussion_r2456356053" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could some logging be added?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/75#discussion_r2456385255" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider omitting the use of 'this' since it is clear that it is referring to the instance variable.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/109#discussion_r2473794630" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks -- Good catch!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/109#discussion_r2473821016" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Update the saved image in the directory.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/109#discussion_r2473837296" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
AC -&gt; IN**: new Internship(...)
'''
As a new internship object is created
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/109#discussion_r2474197827" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
participant "&lt;&lt;class>>\nDashboardUi" as DUi
'''
Add a \n here
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/175#discussion_r2484458801" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

'''suggestion
        return new InternityException("Invalid username command.\nUsage: username NEW_USERNAME");
'''

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/175#discussion_r2484469777" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Perhaps can add some JavaDoc comments here.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/82#discussion_r2452467762" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Good point! Have replaced with logger.severe("Error executing Add Command: " + e.getMessage());
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/82#discussion_r2452468322" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Rectified
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/82#discussion_r2452469102" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Done, thanks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/86#discussion_r2459159983" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks for pointing it out, updated.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/86#discussion_r2459161043" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Have improved the Ui print to be in a table format, like the ListCommand.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/86#discussion_r2459162520" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Sure
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484789512" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks, somehow the auto-format made it this way instead.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484794934" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Updated
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/189#discussion_r2484795757" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Done and yep! :)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/195#discussion_r2486918072" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Good spot, thanks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/195#discussion_r2486919034" expanded>
<div slot="header">

**19 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

That's odd. I have re-saved them again. Is it better now?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/1#issuecomment-3332151092" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/2#issuecomment-3332151291" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/131#issuecomment-3479146214" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

This behaviour is intended; there is also no need for restrictions on whitespaces for usernames.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/171#issuecomment-3480580073" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Resolved.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/issues/168#issuecomment-3480593553" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Resolved.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 37. CHEW.. WEI `@enwei29` (**8** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/8#discussion_r2409786167" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Activity class looks clean and neat, well done!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/8#discussion_r2409793910" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

better if the command name is "add" to keep CLI verbs consistent
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/8#discussion_r2409807370" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Use new ArrayList&lt;>(MAX_RECORDS) instead of Activity[] for simpler functions like adds/deletes
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/11#discussion_r2416057800" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good refactoring of changing line to LINE for constants
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/11#discussion_r2416060185" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job changing to CLI verb 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/30#discussion_r2428037280" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good usage of assertions
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/31#discussion_r2428038816" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good usage of logging
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/39#discussion_r2429862077" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good usage of target assertions
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/105#issuecomment-3457919391" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Great job on DG and UG update!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/187#issuecomment-3477964622" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Well done adding javadocs for the 3 commands!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/198#issuecomment-3481730457" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Well addition to the PPP
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/203#issuecomment-3484000124" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

good addition to README.md
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 38. MUAD..TAFA `@muadzyamani` (**8** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/51#discussion_r2422769210" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice addition using a dedicated `AddCommandException`, which will soon be implemented by the rest of the team for other commands.You could add brief Javadoc comments for each constructor so that it is better explained.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/51#discussion_r2422769284" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would changing `0.0f` to `0.0` be better for consistency with the `double` type? Since the fields are declared as `double`, using `0.0` would avoid mixing `float` and `double` literals and keep the code style perhaps more uniform. Otherwise, the initialization and structure look quite solid.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/68#discussion_r2432171459" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great, LGTM! I see that the refactored code looks cleaner now.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/68#discussion_r2432319675" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I've checked and seems to be alright after the refactoring 👍 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/68#discussion_r2432328053" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I see that you've created a package called `storage`, interesting name choice. What was your reason?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/77#discussion_r2441850487" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM, great addition. We should have the foundation for the UserGuide now.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/156#discussion_r2468736258" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should be a bit mindful of the spacing following the coding conventions, other than that LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/246#discussion_r2483734904" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice, it's consistent with our actual release file name now
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/59#discussion_r2429588557" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Yep, got it! @aydrienlaw will be continuing the refactoring with a new `Command` class.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/9#issuecomment-3341109354" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

LGTM, merging this in
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/12#issuecomment-3350390110" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

LGTM, resolves #3. Merging this.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/41#issuecomment-3379233793" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Resolves #32 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/55#issuecomment-3395782464" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Thanks @saheer17 for the feedback and review! I've created helper functions such as `updateBudgetAfterMark` and `updateBudgetAfterUnmark` as suggested. Also, the command parsing is now more robust, do take a look at the screenshot of the updated output, now able to accept inputs that contain spaces and capital letters such as ` Mark 1`.

<img width="643" height="263" alt="image" src="https://github.com/user-attachments/assets/1b51059d-c924-463e-9e45-f6ca05667b68" />

</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 39. JEWE.. LIM `@Jeweljace` (**7** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/39#discussion_r2417235638" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think it should be removing "Swim (30 mins)" instead of "Swim 1km"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/88#discussion_r2451524272" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

great tests 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/89#discussion_r2452199519" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

just a sudden thought but would it be good to add in calorie recommendations? for example if the goal the mother sets is drastically too low/high maybe we can prompt a recommendation message + a confirm message (yes-> set input as goal; no-> let mother set another goal)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/100#discussion_r2466679376" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great SRP. Moving the welcome/prompt + I/O into Ui keeps concerns clean and makes it easier to test and later swap UIs
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/102#discussion_r2467604191" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great SRP!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/114#discussion_r2471741622" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great move 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/208#discussion_r2487435809" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great! it is more clear now
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/33#issuecomment-3406611153" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Closed by Add workout v1 #34 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/90#issuecomment-3452785936" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Closed by #95 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/91#issuecomment-3452788221" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Closed by #95 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/92#issuecomment-3452789770" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Closed by #95 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/93#issuecomment-3452790440" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Closed by #95 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/94#issuecomment-3452791376" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Closed by #95 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/97#issuecomment-3454323186" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

Closed by #98 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/207#issuecomment-3481458336" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Great check, closes issue where user is able to input "|" resulting in storage error (entry does not show after reload)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/130#issuecomment-3482122224" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

New pdf in correct format will be uploaded for final version
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/178#issuecomment-3482124090" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

New pdf in correct format will be uploaded for final version
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/115#issuecomment-3482188971" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

Unlikely that user will accidentally overwrite her weekly goal. If she does not have the intention to set a new goal, he will not type "workout goal &lt;minutes>". In the rare event she does accidentally overwrite, she can always refer to her previous set workout goal as past workout goals are saved and can be viewed using the list command. She can then set her weekly goal to the previously overwritten value. Adding in y/n may annoy users in the event they wish to overwrite their goal and they have already typed out the command but they enter something other than "y" and the program gives them an error. They then have to go through the whole process again. Users have more chance to input --> more chances to input garbage --> more chances for the program to crash. Therefore I think this y/n is not needed due to users being able to view workout goal history. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/176#issuecomment-3482193930" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

Fixed by #183
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/143#issuecomment-3482197327" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

Fixed by #210 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/172#issuecomment-3482201764" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

Fixed by #210 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/169#issuecomment-3482203147" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

Fixed by #210 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/146#issuecomment-3482279214" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

This is intentional so that user can view the past workout goals that they have set. The most recent workout goal that is within the week will be the current goal. Will elaborate in UG that this feature is intentional. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/issues/163#issuecomment-3482507720" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Unable to replicate error
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 40. NITI..ITIN `@nitin19011` (**7** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/69#discussion_r2428870605" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good idea to clean up the unused portion of the code
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/183#discussion_r2470453003" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for adding these relavent user stories
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/183#discussion_r2470454875" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

It was a good idea to rename this for clarity
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/195#discussion_r2474210142" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This looks robust. good job
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/274#discussion_r2485591849" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for adding the test cases. They provide extensive test coverage
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/276#discussion_r2485894957" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

thanks for adding the tips
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/281#discussion_r2487148377" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for fixing this
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/86#issuecomment-3415906333" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/112#issuecomment-3426951386" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/279#issuecomment-3480756946" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Looks good, thanks 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 41. JOSH.. YUI `@tam308` (**7** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/25#discussion_r2418583382" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This loop could be abstracted into a method called getActivitiesForDate for readability
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/25#discussion_r2418587060" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

well done on handling the edge cases
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/32#discussion_r2428647145" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

duplicate check here with the assertion and the IllegalArgumentException
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/32#discussion_r2428648338" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Consider using a dedicated expense class rather than 3 ArrayLists
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/34#discussion_r2428661049" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

consider using a dedicated expense class rather than maintaining 3 ArrayLists
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/34#discussion_r2428666313" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

assertion and exception thrown here serve the same purpose, maybe can reduce to one check only
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/37#discussion_r2428672819" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

handle budget here is lengthy, consider abstracting methods for readability
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/19#issuecomment-3386219459" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Closing PR due to bug where new branch commits are not reflected.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/20#issuecomment-3386250939" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Closed due to bug infinite loop "Checking for the ability to merge automatically..."
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/25#issuecomment-3388413684" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Overall good implementation of the view commands with clear and functional logic. There might be some opportunities to refactor into methods to improve readability.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/28#issuecomment-3394680714" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Well done on the user guide, structure is clear and easy to follow. Maybe sample output for all cases can be added
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/32#issuecomment-3401112289" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

good and extensive use of assertions and logging!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/34#issuecomment-3401134408" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

excellent test coverage and extensive use of assertions and logging!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/37#issuecomment-3401155545" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

Nice addition of budget handling to main, just needs refactoring to increase readability 👍 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/43#issuecomment-3414160974" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

good use of assertions and logging!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/55#issuecomment-3437673351" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

Well done on the developer guide for your segment!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/57#issuecomment-3441360122" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

nicely explained developer guide 👍 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/63#issuecomment-3446248713" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

clean UI class!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/85#issuecomment-3449681907" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

well done with robust error handling, clean coding structure!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/109#issuecomment-3459486421" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

nice and clean diagrams
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/116#issuecomment-3468629598" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

nicely written
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/120#issuecomment-3471324934" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

nice
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/issues/130#issuecomment-3483760885" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

find with no keyword functions same as list as stated in UG
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 42. NGUY.. DUC `@k1b1t0` (**7** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/14#discussion_r2418615695" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

default is false, no need to
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/14#discussion_r2418618775" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This create many separators
can just print 2 separatos with list of flashcards
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/14#discussion_r2418620734" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should make every Ui's methods static
So that don't need to create instance of Ui
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/20#discussion_r2429313680" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Avoid all the magic string, extract them into Messages 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/20#discussion_r2429315471" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Also create function in UI
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/20#discussion_r2429320755" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

should make it run next flashcard when run "ans", but not really important
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/41#discussion_r2477830787" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should use 3-part naming convention for the test methods (&lt;methodToTest>_&lt;input>_&lt;result>)
And all the other tests too
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/19#issuecomment-3400944619" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

It works
But I only see error handling in removing flashcards, not adding 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/19#issuecomment-3400950726" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

also the regression testing doesn't include your new updates/changes
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/20#issuecomment-3403739179" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Your runtest.bat still have error please fix it
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/87#issuecomment-3477482394" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

You added Message classes but still use the old Ui's methods
Also can put add, remove messages into 1 class like flashcard messages because they don't have too many messages 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 43. TAN ..NDEN `@ZT712002` (**6** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/19#discussion_r2425856030" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Instead of doing this, we can abstract this into another level for a help guide for future iterations. Other than that, this looks great, but make sure to update this when for the other commands aka 'meeting', 'user' & 'policy'
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/20#discussion_r2425862635" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great use of REGEX here. Maybe for future iterations we can keep all relevant REGEX as an enumeration.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/20#discussion_r2425873522" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Policy Name might be problematic with regards to Code Quality. We should not obfuscate the Policy Number with the naming
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/23#discussion_r2427887858" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could this be abstracted to a static FINAL variable instead?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/23#discussion_r2427888213" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could this be abstracted to a static FINAL variable instead?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/23#discussion_r2427888565" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Great use of static variable to abstract away the meeting regex
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/14#issuecomment-3389024902" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Solved with #16 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/27#issuecomment-3419252793" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Looks good to me, I reccomend using Java's Logger Utility to for another layer of defensive coding
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/32#issuecomment-3424482395" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

LGTM!, great work on logging and assertions
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/35#issuecomment-3430360619" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Done with #36 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/38#issuecomment-3442592109" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

done with #39 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/111#issuecomment-3476329950" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Fixed with #121 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/119#issuecomment-3476333826" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Fixed with #121 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/83#issuecomment-3476359975" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

done with #121 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/87#issuecomment-3476394150" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Done with #122
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/114#issuecomment-3477956391" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

fixed with #121
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/129#issuecomment-3477995094" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

Fixes #116 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 44. ADRI.. HNG `@aydrienlaw` (**6** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/58#discussion_r2428405018" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I'm curious why we're using an exception for an empty list. Isn't this a normal state rather than an error?
Would something simpler like this work instead?

```
if (expenses.isEmpty()) ``{``
    showListUsage();
    return;
``}``
```


</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/58#discussion_r2428412200" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The Javadoc mentions "invalid parameters or unexpected runtime errors", but we're using this for empty lists, which seem like normal, valid states. Should we update the docs to match actual usage?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/58#discussion_r2428435003" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

There seem to be two different messages for an empty list of messages:

1. Exception: `"No expenses so far."`
2. UI method: `"No expenses added so far."`

Could we standardise these?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/86#discussion_r2445973691" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I see that you’re saving after every command execution. Would it make sense to save only after mutating commands (e.g., `add`, `delete`)? That might help reduce unnecessary disk writes and improve performance.

Maybe an approach like introducing a flag, such as `command.isMutating()`, could help decide when to save. Alternatively, save once on `bye`.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/86#discussion_r2445976021" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I noticed we’re comparing doubles directly.

Would it be more robust to include a delta, e.g., `assertEquals(expected, actual, 1e-9)` to account for floating-point precision differences?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/86#discussion_r2445977812" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice use of assertions for defensive checks!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/68#discussion_r2432844017" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks for the comment! I placed `ExpenseManager` in the `storage` package because it currently handles both in-memory data management and (potentially) persistence-related logic. It acts as the main interface between commands and data storage.

That said, I’m open to renaming or restructuring if we later separate data persistence from runtime management.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/14#issuecomment-3358888355" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/106#issuecomment-3435799166" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/171#issuecomment-3457993218" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/187#issuecomment-3467915641" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/issues/207#issuecomment-3475879854" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

It seems like the tester may have misread the Developer Guide - the manual test states to **press** `Ctrl+Z`! Not to type it into the application CLI.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/issues/203#issuecomment-3475885138" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

This is the correct error message for non-numeric inputs. Perhaps a tweak to the error message will suffice.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/issues/238#issuecomment-3475891402" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

While neat to have, it does not necessarily add much value to an average user. Perhaps this can be postponed to post `v2.1`!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/issues/217#issuecomment-3478067760" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

The team is unable to reproduce this result - perhaps it is an isolated case?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/259#issuecomment-3479776946" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/267#issuecomment-3482640804" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 45. FOO ..KANG `@fookang` (**5** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2447008188" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Missing : in front of BufferedReader
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2447028220" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Parser shld return Session first, then you will need to call getCourse Method from session class to get the required course before you can get the matchingCourse through the loop.
        
        
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2447033248" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Validate format is not a valid method in DataParser.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2447034384" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Validate format is not a valid method in DataParser.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2447045600" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You should be self calling loadData methods here.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 46. ZHEN..IWEN `@Kevin88866` (**5** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/94#discussion_r2452584844" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think there should be composition
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/94#discussion_r2452586478" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Do we still need pets, since you have a association to class PetList
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2466021679" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe you don't need to write pets, since you have already a association to the PetList class
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/102#discussion_r2466022190" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Same
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/116#discussion_r2472714978" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Is it correct to have two space inside? I forget
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/38#discussion_r2429120593" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

emm, I use this variable to indicate there is a index, but p.valid = false means there is not a index. what do you mean？
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/124#discussion_r2478351347" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

but if I write like this, it would be something like println
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/17#issuecomment-3368173917" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Good
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 47. SHOU..MOUD `@Ibrashoukry` (**5** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/117#discussion_r2471758826" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/117#discussion_r2471760125" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice work making command name clearer!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/120#discussion_r2472803206" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice documentation for the AddWeightCommand
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/190#discussion_r2484616790" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice improvement making the UI look cleaner
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/190#discussion_r2484630063" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should we add some explanations to what some of the commands do? Like what does only typing `workout goal` or `calorie goal` do?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/126#issuecomment-3476050559" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/189#issuecomment-3477775008" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 48. LAI ..REMY `@MinionWolf` (**4** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/21#discussion_r2429033505" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

good addition of toLowerCase()
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/36#discussion_r2444964661" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

possible to add a test method for listing all the incomes?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/36#discussion_r2444969610" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

you could make this into a function. applies for the rest of the code that uses them.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-1/tp/pull/52#discussion_r2450448039" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Remember to add JavaDoc for these methods. Applies for the rest of the other code.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 49. BREN.. HAN `@BTslayer761` (**4** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/75#discussion_r2444873427" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This should be lecture not exam for the JavaDocs
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/75#discussion_r2444876166" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This one should be tutorial not Exams
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/77#discussion_r2445383815" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Should specify the type of exception it throws
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/95#discussion_r2465823995" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would it be better to just have 1 sequence diagram and use that as an example for all check commands
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/74#discussion_r2444885892" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

I am going to implement a function which will clear all tasks past their deadline when the ASTRA starts up.
So daysBetween should never be &lt; 0. (Assertion)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/176#discussion_r2483742746" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Fixed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/16#issuecomment-3368226003" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Completed with commit [f211ac2](url)

Added a task class as well (subclass of Activity) to track tasks,hw,assignments etc.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/13#issuecomment-3368236344" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Completed with commit [8e149d0](url)

Including both activity package(skeleton of all classes) done with commit [f211ac2](url) and command package(skeleton of all command classes) done with commit [03e1f3a](url)



</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/62#issuecomment-3404922194" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Looks good. There were no issues in terms of the styling and the functions relating with exams works fine

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/70#issuecomment-3418422524" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

A lot of your checks are don't pass
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/72#issuecomment-3419249791" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Looks ok
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/66#issuecomment-3421913307" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Completed at commit [b3560e5](url)

Tested with JUnit test at commit [2e82263](url) 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/91#issuecomment-3451137976" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

For the Class diagram should separate out some commands because not all commands are a subclass of an abstract class
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/92#issuecomment-3451142520" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/101#issuecomment-3456308896" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/102#issuecomment-3456892227" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/114#issuecomment-3468497265" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/174#issuecomment-3476191775" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

lgtm. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/143#issuecomment-3476383332" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

Invalid Issue. The error was caused by giving wrong input format. did /by and /priority twice. So the entire String after the first priority was taken in as an input for priority
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/155#issuecomment-3476386416" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

UG has mentioned that both HHmm and HH:mm are valid input formats
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/134#issuecomment-3476416264" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

Resolved with commit [ad51331](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/176/commits/ad513319025c8b5a3c61d4ab2a66cf954007f671)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/139#issuecomment-3476418797" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

resolved with commit [15eaec2](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/176/commits/15eaec2d165b0277c1ce18abaedbd793a48a00a3)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/141#issuecomment-3476419531" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

Resolved with commit [9365d6c](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/176/commits/9365d6cf78d65a9018235b287afa0033fb1e7f37)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/152#issuecomment-3476420555" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

Resolved with commit [6719db9](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/176/commits/6719db92c041bbd8422cf77eb8286dc810d7ab62)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/148#issuecomment-3476427212" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

Astra does not contain a feature for checkexam &lt;day>. checkexam will list all exams. There is no filter input implemented.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/178#issuecomment-3477393919" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

Looks good
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/129#issuecomment-3477958571" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

Resolved with commit [57762d9](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/57762d91b86a0eac1f53fcce30eb47a3d9b737ff)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/165#issuecomment-3477959051" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

Resolved with commit [d453cfd](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/d453cfdab22fbcdb16294778e36791360338fab7)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/173#issuecomment-3477959694" expanded>
<div slot="header">

**29 :octicon-comment:** %%(other comment)%%
</div>

Resolved with commit [b370513](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/b37051395d68f09e08831e6a44fee0dea6980fd4)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/185#issuecomment-3479662510" expanded>
<div slot="header">

**30 :octicon-comment:** %%(other comment)%%
</div>

Good changes but i want to check both activity_package.png and activity_component.png are the same
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/189#issuecomment-3481266757" expanded>
<div slot="header">

**31 :octicon-comment:** %%(other comment)%%
</div>

Nice implementation to handle corrupted data in data files
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/193#issuecomment-3481307381" expanded>
<div slot="header">

**32 :octicon-comment:** %%(other comment)%%
</div>

Looks good
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 50. OOI .. REE `@Wrooi` (**4** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/30#discussion_r2418810634" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

if(input.isEmpty()) should have spaces inbetween. Rmb to refactor (ctrl+shift+alt+L) your code when you done.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/107#discussion_r2471429947" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job neatening the command summary's formatting to make it more legible for the user!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/107#discussion_r2471431999" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good update on all the anchor links and ensuring they work!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/107#discussion_r2471432935" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Is the number listing correctly implemented?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/109#discussion_r2471641579" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Noted, I have made the necessary changes, please re-review.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/171#issuecomment-3477841848" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

Check DG/UG if intended or not, don't change code. DG change the user stories to only top 5.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/163#issuecomment-3477853422" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Create exception component in DG
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/157#issuecomment-3477855227" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Specify in UG English Alphanumeric + symbol allowed only
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/158#issuecomment-3477855582" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Specify in UG English Alphanumeric only
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/154#issuecomment-3477864022" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Carrot is industry standard. State clearly in UG.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/151#issuecomment-3477865926" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Check with Joanne if this is considered sabotage.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/148#issuecomment-3477867798" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Future date is not allowed. Update in DG and UG. Code also needs clearly feedback msg.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/139#issuecomment-3477872864" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Ask Joanne if this is considered sabotage (grammar + chinese).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/137#issuecomment-3477875992" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

Change to float + decimal point show only until 2 max OR state whole numbers ONLY in DG/UG (future iterations).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/130#issuecomment-3477881528" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Update UG/DG to state this is allowed because "flexibility of user naming convention"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/215#issuecomment-3481922623" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

Sabotage, out of course scope
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 51. CHIU.. CHI `@ycdaniel326` (**4** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/81#discussion_r2476256645" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Clear and well-structured diagram that shows the logic flow of command processing clearly. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/81#discussion_r2476260235" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The example given helps the reader more quickly understand how the commands are actually processed, and the logic flow is easy to follow. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/81#discussion_r2476308551" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good to include the design principles. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/81#discussion_r2476323017" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The diagram clearly illustrates the relationship between the classes.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 52. ONG .. YAO `@chongyaoo` (**3** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/158#discussion_r2484893031" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for removing some variables to keep the diagram cleaner and more readable.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/163#discussion_r2485534317" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good spot of the unintended bug. Thanks for fixing firing issue.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/165#discussion_r2486998838" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Thanks for fixing the issue!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-3/tp/pull/85#issuecomment-3467692656" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Good update
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 53. PAVI..ASAN `@Pavithra6-Srinivasan` (**3** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/116#discussion_r2472216334" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think we can use WARNING since we are sticking to INFO or WARNING
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/116#discussion_r2472231784" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

if (commandName != null) ``{``

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/160#discussion_r2478559621" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

we can remove this
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/18#issuecomment-3369880703" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/32#issuecomment-3382231984" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/73#issuecomment-3415765286" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/132#issuecomment-3468082893" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/136#issuecomment-3468240776" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/144#issuecomment-3468340628" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/146#issuecomment-3468368797" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/124#issuecomment-3468386792" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/153#issuecomment-3468498741" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/155#issuecomment-3468511400" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/157#issuecomment-3468594724" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/159#issuecomment-3468618294" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/162#issuecomment-3468670797" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/219#issuecomment-3476429757" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/220#issuecomment-3476430622" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/221#issuecomment-3477441989" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/226#issuecomment-3479178574" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/239#issuecomment-3481221856" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/242#issuecomment-3481604758" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/246#issuecomment-3481782103" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

lgtm
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-4/tp/pull/259#issuecomment-3483944520" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 54. ANG .. BIN `@AWeiBin` (**3** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/77#discussion_r2446729925" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Please remove the dummy assertion
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/77#discussion_r2446730522" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Please keep the logger for Planner 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/76#discussion_r2446737061" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Please ensure that you have obtained permission to use this, as I did not see this dependency approved in the forum.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/176#issuecomment-3479704472" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

I have tested the code and the above mention course are not part of the prerequisite of CS2113. Perhaps the tester provided the wrong module code in this issue

add CS2113 to Y1S1
Prerequisites not met for CS2113. Requires: Prerequisites: [[CS2040C] OR [CS2030, CS2040S] OR [CS2030, CS2040] OR [CS2030, CS2040DE] OR [CS2030S, CS2040S] OR [CS2030S, CS2040] OR [CS2030S, CS2040DE] OR [CS2030DE, CS2040S] OR [CS2030DE, CS2040] OR [CS2030DE, CS2040DE]]
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/172#issuecomment-3479720336" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Similar issue from the tester #174 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/173#issuecomment-3479721857" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

Similar issue from the tester #174
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/184#issuecomment-3479779985" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Since the target audience for this application is freshmen, outdated modules will not be included. Moreover, this module does not appear on the NUS website, which suggests that it may have been renamed to PF111A.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/issues/162#issuecomment-3494571631" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

It is mention in the guide that the targeted audience are freshman hence we will not be implementing the suggestion.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 55. ZHON..AODE `@ZhongBaode` (**3** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/106#discussion_r2446840330" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can you throw a error here instead? to prompt user to key in valid command. Perhaps use an exception
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/106#discussion_r2446842408" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You trim argumentStr while checking too. Perhaps can simplify the code by having argumentStr trimmed at the start
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-3/tp/pull/151#discussion_r2461028874" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good documentation
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 56. AHME..HEER `@saheer17` (**3** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/55#discussion_r2424661338" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You may want to consider encapsulating the expense calculation logic into a helper function. This might improve readability!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/55#discussion_r2424672551" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

You may consider making the command parsing a bit more forgiving by trimming the input and allowing flexible spacing or capitalization (e.g. " Mark 2" )
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/105#discussion_r2454311432" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could refactor this and create a helper method to improve readability!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/54#issuecomment-3394264082" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

@limzerui Thank you for the constructive feedback! I have updated the delete command to be case-insensitive by converting the user input to lowercase prior to parsing. This ensures that variations such as "DELETE 3" or " delete 3" are now handled correctly. Regarding the help messages, I agree with your suggestion regarding including printing of valid range when out of range error is raised. I have implemented that via the parseDeleteCommand(). 

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/55#issuecomment-3395007316" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

The refactoring clearly improves code readability and maintainability , separating parsing logic into parseMarkUnmarkCommand() and introducing MarkUnmarkCommandException were both excellent design choices. The use of assertions, targeted exception handling and detailed logging were done well.

I have two minor suggestions to consider for further refinement:

1. Make command parsing more forgiving . For example, allowing flexible spacing or case-insensitive input such as " Mark 2". This would enhance user experience and prevent unnecessary command errors.

2. Encapsulate expense/budget update logic. Moving the total and remaining balance updates into a small helper method could make the code safer (in case of partial failures) and more maintainable as related logic grows.

Overall, this is a solid and thoughtful improvement to the command , great job!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/56#issuecomment-3396033951" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

Thanks for catching this and updating EXPECTED.TXT!  This keeps the test output consistent with the actual program behaviour. Nice quick fix!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/68#issuecomment-3405660380" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Great work @aydrienlaw!  Code structure, modularization, and command implementations are all clean and consistent. Clear separation of concerns and thoughtful refactoring, everything looks solid.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/73#issuecomment-3416051243" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Nice work @limzerui!  I like how you added the category feature across everything. It is clean, consistent and works great with the UI. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/74#issuecomment-3416059703" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Nice work @limzerui!  Moving the hardcoded bye logic into a proper ByeCommand is a great improvement, much cleaner and more modular.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/77#issuecomment-3417915626" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Good job @limzerui ! Looks like a good foundation for us to work on our User Guide!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/85#issuecomment-3422149991" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Great work on implementing the EditCommand feature! The integration with ExpenseManager and Ui is seamless and the handling of optional fields makes editing flexible and user-friendly.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/88#issuecomment-3424612998" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

Excellent work on the UML diagrams, they arere clean and intuitive. The documentation updates are well-written and provide clear explanations of the features.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/105#issuecomment-3435702911" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

Overall, a very good implementation of the progress bar. I like how intuitive it is for users to understand. Perhaps, you could refactor some logic and add them as helper function to improve readability. Other than that, good job!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/116#issuecomment-3445539531" expanded>
<div slot="header">

**14 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/127#issuecomment-3445540691" expanded>
<div slot="header">

**15 :octicon-comment:** %%(other comment)%%
</div>

Good consideration of edge cases, this significantly improves our test coverage. Keep it up!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/128#issuecomment-3445552134" expanded>
<div slot="header">

**16 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/129#issuecomment-3445554562" expanded>
<div slot="header">

**17 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/138#issuecomment-3449638439" expanded>
<div slot="header">

**18 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/134#issuecomment-3449642571" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

UI Component is comprehensive, good job!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/136#issuecomment-3449643835" expanded>
<div slot="header">

**20 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/138#issuecomment-3450377450" expanded>
<div slot="header">

**21 :octicon-comment:** %%(other comment)%%
</div>

Do remember to add the components regarding your contribution to the UG and DG!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/153#issuecomment-3452228352" expanded>
<div slot="header">

**22 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/168#issuecomment-3457343846" expanded>
<div slot="header">

**23 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/176#issuecomment-3461686144" expanded>
<div slot="header">

**24 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/252#issuecomment-3477987388" expanded>
<div slot="header">

**25 :octicon-comment:** %%(other comment)%%
</div>

Great that you added new test cases accordingly, LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/255#issuecomment-3478037063" expanded>
<div slot="header">

**26 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/257#issuecomment-3478921471" expanded>
<div slot="header">

**27 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/262#issuecomment-3480890194" expanded>
<div slot="header">

**28 :octicon-comment:** %%(other comment)%%
</div>

 LGTM
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 57. YAO ..IANG `@Yxiang-828` (**2** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/63#discussion_r2467974632" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

seems fine to me, so here is where everyone claim credits and describe the features that they have contributed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/63#discussion_r2467984227" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

what do you think about a table of contents?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/6#discussion_r2394025964" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

no you are wrong, copilot. I'm right.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/117#issuecomment-3480660335" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Delete items: delete-project &lt;projectIndex> --confirm or delete-task &lt;projectIndex> &lt;taskIndex> or delete (interactive mode)

Our user guide clearly highlighted that "or delete (interactive mode)" is also an option to delete tasks, hence this issue is due to the lack of understanding of our user guide. I suggest to not make any changes regarding this issue.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/114#issuecomment-3480744855" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

This is an issue with the lack of error-handling messages in our code regarding empty project tasks. I'll fix this.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/125#issuecomment-3481388718" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

 "Fix add command priority/deadline validation
>>
>> - Collect all validation errors instead of stopping at first error
>> - Show clear error messages for empty priority/deadline values
>> - Display multiple errors together in user-friendly format"
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/125#issuecomment-3481451029" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

> wait i think i kinda already solve this issue in my previous pr

alright, i have vetted your change, we can stick to yours, ill use this pr to fix the add command instead
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/113#issuecomment-3481469493" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

this is a valid issue, I will fix the diagram right now
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/129#issuecomment-3481728756" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

looks good now
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/130#issuecomment-3481731359" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

ok removed!

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/103#issuecomment-3482675694" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

> noted that this does not cause a functional error or unexpected error but can be a place for improvement? lower priority on the list, what yall think?

I think this is a bug, we should ensure specific error message given to invalid parameters/subcommands for cases like this.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 58. ONG .. JIE `@yujie-o` (**2** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/100#discussion_r2465334023" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Excellent modularization — the class clearly defines the “data aggregation” responsibility
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/100#discussion_r2465334523" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good use of assertions to ensure defensive programming (list != null, storage != null).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/29#issuecomment-3380307547" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

LGTM ! Remember to include Fixes #&lt;issue_number> (e.g., Fixes #22, Fixes #23) in your commit message so that the corresponding issues are automatically marked as completed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/34#issuecomment-3384963183" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

LGTM !
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/54#issuecomment-3402096186" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

LGTM !
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/105#issuecomment-3454916667" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

Great feature addition: making “feel (1–5)” a first-class field in WorkoutEntry and threading it through usage, storage, and tests is solid. The tests are broad, and the docs/logging are clearer.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/110#issuecomment-3457433810" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

LGTM !
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/111#issuecomment-3457439983" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

LGTM !
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/112#issuecomment-3457445292" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

LGTM !
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/113#issuecomment-3457452306" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

LGTM !
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-3/tp/pull/197#issuecomment-3479129461" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

LGTM !
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 59. ABE .. YIN `@abefqy` (**2** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/50#discussion_r2465199683" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

does this only allow for 1 policy per person to be saved?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/50#discussion_r2465987244" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Got it, no further issues
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/21#issuecomment-3400204207" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Solved with #23 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/27#issuecomment-3419249890" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Looks all good to me!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/29#issuecomment-3450013385" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

solved with #42 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/31#issuecomment-3450013774" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

solved with #43 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/46#issuecomment-3450576831" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Looks all good to me!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/30#issuecomment-3450770713" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

solved with #44 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 60. LI M..EIYI `@limeiy1` (**2** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/77#discussion_r2439066950" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

do you want to consider using Level.WARNING instead of Level.INFO? 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/279#discussion_r2487455452" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Maybe change this line to remove the "(--mode summary)"?
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/138#discussion_r2465077256" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

yes, thanks for pointing it out!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/35#issuecomment-3388069898" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/36#issuecomment-3388077061" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/73#issuecomment-3413860180" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/180#issuecomment-3465915743" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/185#issuecomment-3465916287" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/181#issuecomment-3465918094" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/189#issuecomment-3466670525" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/247#issuecomment-3483998434" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Chose to keep the original naming to allow for more specificity. Only traffic related cases always have a road name associated to them, unlike other cases which might have a location but not a road name.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/issues/231#issuecomment-3484018129" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

From the arrowhead, a CaseManager object is associated with a Case object, so CaseManager has reference to Case
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 61. CHEO.. HAO `@JianHao24` (**2** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/105#discussion_r2474494219" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

This is redundant, zettle auto saves after each command
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/105#discussion_r2474495654" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

refer to zettel class
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/86#issuecomment-3454872810" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 62. MUKH.. ISA `@mukhtarcal` (**2** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/32#discussion_r2472473091" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could add a space after command just for cosmetic consistency, not a big deal.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-1/tp/pull/32#discussion_r2472478904" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Is the space necessary after "flashCard!"?
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 63. JUNG..YEON `@Joannaj00` (**2** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/75#discussion_r2445680655" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would be nice to have a "Ui.printSetUsername(username)" so that the user can see confirmation!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/119#discussion_r2477550580" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

this is minor but If --> if
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/38#discussion_r2417614384" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Did it!! Thank you
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-4/tp/pull/38#discussion_r2417615814" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

But shouldn't the parser still need access to the same InternshipList instance so that it can hand it over to commands? 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 64. PANG..SHER `@ashpasa` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-2/tp/pull/130#discussion_r2484785120" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Is this supposed to be a test file, or to be committed to main branch?
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 65. GORD.. JIE `@gordonajajar` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/51#discussion_r2438035177" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Could add into a util package.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/issues/198#issuecomment-3476391635" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Closed; duplicate of #175 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 66. BRIE..HONG `@blimc1` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/40#discussion_r2429874668" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Good job on checking if the inputted date follows the proper format.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/23#issuecomment-3388032729" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Well done resolving the infinite loop
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/29#issuecomment-3396354032" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Good job on adding assertions!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/40#issuecomment-3402840806" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Overall, nice changes. 👍
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/56#issuecomment-3437734298" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Good job. Hope to see more details in the final version!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/65#issuecomment-3446851301" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

Good job on creating a separate parser class to use more OOP!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/199#issuecomment-3483638420" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Good job on finding and solving the bug!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 67. T. K..SAMI `@t-kandasami` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/118#discussion_r2477020751" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

The diagram looks less complicated and easier to read
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 68. MICH.. ZHI `@Michael-Low` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/190#discussion_r2476915337" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

did you mean to commit this?
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 69. IRWA..NOOR `@irw9n` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/159#discussion_r2485847339" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Nice!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/59#issuecomment-3426611766" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

LGTM!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/106#issuecomment-3471485996" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

LGTM
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 70. JOSH.. TZE `@Ekko-Technology` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/82#discussion_r2447932018" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

I think this sentence is quite redundant HAHAHA
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/17#issuecomment-3377471819" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Fixed with commit 0511eba.

This allows for deadline changes within any Task instance within taskList and exception handling for changing the deadlines of non-Task instances.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/10#issuecomment-3391730674" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Fixed with 6cf44ab
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/64#issuecomment-3418420332" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Fixed in commit [9a7aebb]([9a7aebb](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/70/commits/9a7aebb0b8fae253242e0f63fa8940ffabb16c42))
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/64#issuecomment-3419204576" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Change method to set priority without scanner logic in commit: [a9086c1](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/72/commits/a9086c1fd3f68a065956870023be61d1cffa35c5)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/pull/82#issuecomment-3426305875" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

Overall, code looks good. Variables can be more descriptive.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/64#issuecomment-3446989200" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Add final error checks for priority handling in commit:[ 00d3c3](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/00d3c3de1b813cc9c787500d8e04fda8e0a57d09)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/63#issuecomment-3446992604" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

FIx in commit: [f17de1](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/f17de1113a12166a9496db524a7f6e7e9f0a3e58)

"checkcurrent" displays all upcoming deadlines from the current DateTime and ignores all past task deadlines 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/159#issuecomment-3478989568" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Fix with commit [81db85c](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/183/commits/81db85ce3b071a9caffe1f45b579d04edd2906e8)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/153#issuecomment-3479104218" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Fix with commit [81db85c](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/183/commits/81db85ce3b071a9caffe1f45b579d04edd2906e8)
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 71. GU M..UJIA `@gumingyoujia` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/59#discussion_r2429486817" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Can consider move the parser methods for add, delete, set budget, mark and unmark commands in expenseManager class to this parser class for better separation of concern. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/58#discussion_r2428618885" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks for the suggestion, I have changed the code to handle this way. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/58#discussion_r2428621058" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks for pointing that out! I have standardized the message to "No expenses added so far."
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/58#issuecomment-3402425264" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

resolves #52
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/45#issuecomment-3402430002" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

resolves #35
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/44#issuecomment-3402432670" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

resolved #28
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/13#issuecomment-3402435717" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

resolve #6 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/96#issuecomment-3432680769" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Resolves #95 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T11-2/tp/pull/169#issuecomment-3457214247" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Resolves #170 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 72. SEAH..G LI `@seahsongli` (**1** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/23#discussion_r2450655461" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** (commented on others PR)
</div>

Would there by any reason to not use the class method parseListCommand() to instantiate? 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/16#issuecomment-3404774310" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Looks good!

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/pull/26#issuecomment-3435920374" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Great work man :)
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 73. YEOH..EONG `@Yeoh-Soo-Leong` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-2/tp/pull/129#issuecomment-3477456415" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

Added current_semester command
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 74. LIU ..QUAN `@LJQ2001` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/64#discussion_r2450795614" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Removed the enableAssertions
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/64#discussion_r2450796853" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Removed the enableAssertions
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/52#issuecomment-3414307769" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Thanks a lot.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/69#issuecomment-3441379500" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Add simple checks for now will add more once more UI code is developed

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W10-1/tp/pull/162#issuecomment-3480024007" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Had to also edit the test cases due to the changes of the Storage
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 75. REVA..MIKA `@samika2005` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/74#issuecomment-3448952496" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

efficient enhancement!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/89#issuecomment-3450178864" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Looks good!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/95#issuecomment-3456072674" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

great!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/99#issuecomment-3456639320" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

good!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/102#issuecomment-3457372680" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

great!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/104#issuecomment-3457883913" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

lets go!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/115#issuecomment-3466679570" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

looks good!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/116#issuecomment-3468629534" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

perfect!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/118#issuecomment-3468750598" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Great!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-4/tp/pull/189#issuecomment-3478041170" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

Looks good!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 76. ONG .. KAI `@EggsKay` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/50#discussion_r2465857562" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

yup currently the implementation only allows for saving of 1 policy per person, future implementations will allow for more.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/9#issuecomment-3393999459" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Solved with #18
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/28#issuecomment-3420397891" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Looks good no issues found
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/42#issuecomment-3449868757" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

nice use of nric to search for the client. Maybe add some defensive coding to this portion.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/43#issuecomment-3449880773" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

nice use of assertions to make the code more defensive, the rest seems good no issues found
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/44#issuecomment-3450078104" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

no issues found for me 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/37#issuecomment-3451696255" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

solved by #50 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/48#issuecomment-3451701607" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Looks good, just handle the merge conflicts and its good to go.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/125#issuecomment-3477547842" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Solves #117 #106 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/117#issuecomment-3477548201" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

solved by #125 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/106#issuecomment-3477548416" expanded>
<div slot="header">

**11 :octicon-comment:** %%(other comment)%%
</div>

Solved by #125 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/110#issuecomment-3477887415" expanded>
<div slot="header">

**12 :octicon-comment:** %%(other comment)%%
</div>

solved with #126 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/99#issuecomment-3477887620" expanded>
<div slot="header">

**13 :octicon-comment:** %%(other comment)%%
</div>

solved with #126 
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 77. SHEN.. TAY `@shennontay` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/80#discussion_r2442780966" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Thanks, I've adopted your suggestions!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-3/tp/pull/190#discussion_r2477341891" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

whoops i didn't, thanks for pointing it out!
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 78. KENN..N WI `@Kurokishi592` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/8#issuecomment-3368149216" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

Fixed with commit [eb0539a ](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/eb0539aa7b954932229367cb34eb86e7bf67489f). 

This includes the rough structure of the project from commit [f81e88d](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/f81e88dfe07773259f4cc2deedd8646425d655ac) and addition of the main, parser and ui class from commit [9e93f29](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/9e93f298a91898be8c6932535c9237e62847dbc8).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/36#issuecomment-3381194095" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Done under commit [139a3e5](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/139a3e5cfd25aa7601d4d8858a587f6df7a47cac)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/15#issuecomment-3381196734" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Done under commit [139a3e5](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/139a3e5cfd25aa7601d4d8858a587f6df7a47cac)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/33#issuecomment-3381199240" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Done under commit [139a3e5](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/139a3e5cfd25aa7601d4d8858a587f6df7a47cac)
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/34#issuecomment-3381202535" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Somewhat did some under commit [139a3e5](https://github.com/AY2526S1-CS2113-W12-1/tp/commit/139a3e5cfd25aa7601d4d8858a587f6df7a47cac), but it can be even neater.

Will go back on Ui stuff after all critical features and bugs are fixed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/34#issuecomment-3401504781" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

e.g. days use enumeration need to update that

basically 2 objectives:
- clear to users what input to write
- make the help command short and concise
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/37#issuecomment-3401915711" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Added under commits [c4b14e6](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/52/commits/c4b14e6caf3d11386fe8efdbd9e58f1724da38f7), [589b2a8](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/52/commits/589b2a800615deb5d8e618df2267b2ea83b9f958), and [e54c96b](https://github.com/AY2526S1-CS2113-W12-1/tp/pull/52/commits/e54c96b0776bca7d28341e9e2c07098ea856dd92).
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/54#issuecomment-3402878638" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Fixed under PR #57  
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/69#issuecomment-3430298979" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

Added via PR #82 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-1/tp/issues/93#issuecomment-3452455317" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

PR #97
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 79. GAN ..HIEN `@asytrix99` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/51#discussion_r2432715624" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed, will make those changes, thank you for pointing out!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/51#discussion_r2432716029" expanded>
<div slot="header">

**2 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed, will make those changes, thank you for pointing out!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442450579" expanded>
<div slot="header">

**3 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed, will make the necessary changes.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442450596" expanded>
<div slot="header">

**4 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed, will make the necessary changes.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442450781" expanded>
<div slot="header">

**5 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed, will make a separate 'DataParser' class to handle solely parsing of data.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442450924" expanded>
<div slot="header">

**6 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442451284" expanded>
<div slot="header">

**7 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Originally changed it back to the classic concatenating way due to Java support, but issue fixed, will change back to this.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442451321" expanded>
<div slot="header">

**8 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Noted, thanks.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442451380" expanded>
<div slot="header">

**9 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed, will make the necessary changes.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442451451" expanded>
<div slot="header">

**10 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Noted, thanks.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442451514" expanded>
<div slot="header">

**11 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Noted thanks.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442468586" expanded>
<div slot="header">

**12 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Good catch! Will make changes.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/63#discussion_r2442468626" expanded>
<div slot="header">

**13 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Good catch! Will make changes.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2448279834" expanded>
<div slot="header">

**14 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Good eye! Will make the changes.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2448283673" expanded>
<div slot="header">

**15 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed. Will add in these details.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2448286172" expanded>
<div slot="header">

**16 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed. Will add in the necessary details.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2448287441" expanded>
<div slot="header">

**17 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed. Will add in the necessary details.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/pull/71#discussion_r2448290641" expanded>
<div slot="header">

**18 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Agreed. Will add wrap the details within this method.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-2/tp/issues/139#issuecomment-3479146644" expanded>
<div slot="header">

**19 :octicon-comment:** %%(other comment)%%
</div>

It does not hinder the reader, then not considered, ref: CS2113 website:

`Minor grammar errors: You may categorize a minor grammar bug as severity.VeryLow type.DocumentationBug. And, a grammar bug can be marked as response.NotInScope if it doesn't hinder the reader.`
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 80. XYLO..HONG `@xylonc` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/28#discussion_r2434724910" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

thanks for helping me point it out , I changed it to no use of mockito anymore and built successfully 

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/21#issuecomment-3401635729" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Realised i need to use a different branch to create PR so closing this one
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/pull/48#issuecomment-3427214582" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

fixed the issues for build error
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-2/tp/issues/103#issuecomment-3478122570" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

noted that this does not cause a functional error or unexpected error but can be a place for improvement? lower priority on the list, what yall think?
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 81. VENK..THAN `@shira421` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W13-1/tp/pull/51#issuecomment-3413264173" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

Update JDocs for command files
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 82. TOH ..IZEN `@Izen9835` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/pull/58#issuecomment-3459460032" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

lgtm

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/pull/76#issuecomment-3459479885" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

gave issues after merging with main, even though indiv PR checks passed, hence reverting
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/pull/83#issuecomment-3459810087" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Accidentally didn't resolve the Athlete.java thing yet so it is caught up here also
origin: PR #79 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/pull/79#issuecomment-3460031998" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

being fixed in #85 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/116#issuecomment-3478936012" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

I will just make the names auto capitalised
excluding individual words such as 's/o'

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/137#issuecomment-3478945970" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

this exception is already accounted for
the correct order of command expected is given when the wrong parameter input is given.

```
/newsession morning 0001
    ____________________________________________________________
    InvalidCommandException: Unknown command: 'Athlete ID must be 4 characters long.'. Type /help to see available commands.
    ____________________________________________________________
    ____________________________________________________________
    Command: /newsession
    Usage: /newsession <Athlete ID> <Description>
    Description: Adds a session to the specified athlete with a description
    Example: /newsession 0001 Legs
    Note: Athlete ID = 4 digits
    ____________________________________________________________
```

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/134#issuecomment-3478951295" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

It's not expected that &lt;exercise description> needs to be in upper case anyway
For the names, issue fixed when fixing #116 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/120#issuecomment-3478955414" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

Although weird, the user input for exercise description should not necessarily exclude a numbers only exercise description.
just a strange thing to nitpick though
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/119#issuecomment-3478980442" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

I am just gonna add checks such that total athletes does not exceed 9999, total sessions does not exceed 999 and total exercises does not exceed 99
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/191#issuecomment-3483437285" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

not sure if it's just me, will test again
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 83. NOCH..ANSH `@sivanshno` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-4/tp/pull/1#issuecomment-3305218619" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

Rejected because never change description
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 84. CAI ..NGZE `@andrewcai8` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/20#discussion_r2428006371" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

Acceptable for V1, will discuss in next meeting for adjustments needed for v2.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/6#issuecomment-3400455536" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Done with #19
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/25#issuecomment-3400465280" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Done with #20 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/49#issuecomment-3454628440" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

#48 Done
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/54#issuecomment-3456406069" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Looks good!
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/47#issuecomment-3467120036" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

#53 Completed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/pull/70#issuecomment-3467380966" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

Looks good!

</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/84#issuecomment-3483635424" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

#154 Fixed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/101#issuecomment-3483657866" expanded>
<div slot="header">

**9 :octicon-comment:** %%(other comment)%%
</div>

#155 fixed
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W12-2/tp/issues/96#issuecomment-3483658148" expanded>
<div slot="header">

**10 :octicon-comment:** %%(other comment)%%
</div>

#155 fixed
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 85. HANS..OONG `@ChangIkJoong` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/pull/22#issuecomment-3368998118" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

works now. everybody pull from this and update your projects to work on it further.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/32#issuecomment-3380776436" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

done, completed last week. 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/53#issuecomment-3422457998" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Completed, please check the new latest request.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/113#issuecomment-3481827655" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

Adjusted in new branch and pull-request.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/121#issuecomment-3482135651" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Completed in commit: #182 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/132#issuecomment-3482170261" expanded>
<div slot="header">

**6 :octicon-comment:** %%(other comment)%%
</div>

Fixed in commit #183 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/155#issuecomment-3482179151" expanded>
<div slot="header">

**7 :octicon-comment:** %%(other comment)%%
</div>

fixed in #183 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/154#issuecomment-3482270726" expanded>
<div slot="header">

**8 :octicon-comment:** %%(other comment)%%
</div>

#184 , solved !
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 86. CHEN..EFAN `@W1ndB10w` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/issues/110#issuecomment-3482247818" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

Not an issue.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/issues/135#issuecomment-3482267861" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

Similar issue as #114 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/issues/105#issuecomment-3482508123" expanded>
<div slot="header">

**3 :octicon-comment:** %%(other comment)%%
</div>

Fixed this issue in **v2.1**.
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/issues/147#issuecomment-3483278645" expanded>
<div slot="header">

**4 :octicon-comment:** %%(other comment)%%
</div>

This is the same issue as #74 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/issues/92#issuecomment-3483390017" expanded>
<div slot="header">

**5 :octicon-comment:** %%(other comment)%%
</div>

Invalid issue.
This should be `filter` command (instead of `list` command).
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 87. HUAN..NGRU `@Amanda-HUANG88` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-2/tp/pull/130#discussion_r2484790328" expanded>
<div slot="header">

**1 :octicon-git-pull-request::octicon-comment:** %%(commented on own PR)%%
</div>

To the main branch. Since I have modified some methods in the storage file, the corresponding testing block should be changed, or it cannot pass the gradle check.
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 88. COKE.. CAN `@Sheeeesh-code` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/119#issuecomment-3477852198" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

Actually guys for this one I tried and it after 99 it will start creating Exerçise ID with Id of 100, then 101 and keep going but we can't access it (cuz Exerçise id need to be 2 digit to be accessible ) so there will be no collision. I let the issue open if someone wants to do something with it 
</panel>

<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/issues/164#issuecomment-3477884499" expanded>
<div slot="header">

**2 :octicon-comment:** %%(other comment)%%
</div>

For me It works if someone can confirm. SO I think it's false bug or an error of the tester?
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 89. PACZ..LIAN `@sandrej09` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-T10-3/tp/issues/30#issuecomment-3483340138" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

now can by user code or user nick
</panel>

</panel>


<panel type="info"  collapsed>
<div slot="header">

### 90. MA Z..HENG `@mazh25` (**0** comments)
</div>


<panel  popup-url="https://github.com/AY2526S1-CS2113-W14-1/tp/pull/58#issuecomment-3426461942" expanded>
<div slot="header">

**1 :octicon-comment:** %%(other comment)%%
</div>

all tests passed, ready for review, close #57 
</panel>

</panel>
