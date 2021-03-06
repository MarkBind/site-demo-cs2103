In this semester, we build a scaled-down version of ‘a Siri for keyboards’. i.e. a tool that can accept natural language commands via keyboard. This is for folks who can type fast, spend most of the time near a computer, and prefer typing over mouse/voice commands.

It is ‘scaled down’ in the following ways:

1.  It handles only commands related to managing the user's schedule and todo tasks.
2.  The commands will not be truly ‘natural language’. The command format will be flexible, but still quite structured. NLP (Natural Language Processing) is not required.

Let us use the generic term 'Task Manager' to refer to this product. You should give it a different name yourself.

**Problem outline**: We are bombarded with ‘things to do’ continuously. Some things need to be done during specific times (e.g., attend meeting), some have deadlines (e.g., submit report), and others are simply ‘to be done someday’ (e.g., read ‘Lord of the Rings’). The pile of todo items accumulates and weighs heavily on our mind at times. Sometimes things go out of control and we forget to do certain things on time.

**Solution outline**: The software should help user to put these todo items into a systematic process that tracks them and helps the user to decide what to do and when to do things so that the user doesn’t have to remember the todo items.

**Target audience**: There are many similar software that tackles some aspect of this problem (todo lists software, calendar software, GTD software). Because it is a crowded product space, our strategy is to become a niche player by targeting a specific user group. Our target users are people like Jim whose workflow is described below.

<img src="images/Jim at his computer.png" style="width: 500px;">

Most of Jim’s todo items arrive as emails. This is how Jim processes his emails.

1.  Decides what is the follow up action required by that email.
    
    *   If it can be done immediately, he does it right away (e.g., just reply to the email) and ‘archive’ the email (i.e. move it out of inbox).
    *   If it cannot be done immediately, he schedules the follow up action in his calendar and archives the email. If he cannot decide a good time to do the action, he simply schedules it in a relatively free area in his calendar.

3.  When Jim is free to do some work, he looks at his calendar and picks up something that he can do at that time. Once the task is done, he marks it as ‘done’. If there is a further follow up action required, he schedules it in the calendar.
4.  Jim periodically reviews the calendar to pick items that could not be completed and need to be rescheduled or discarded as ‘cannot do’.
5.  Todo items not arising from email are dealt similarly by entering them in the calendar.

As you can see from the above workflow, Jim’s inbox is almost empty most of time (%%cf [Inbox Zero](http://whatis.techtarget.com/definition/inbox-zero)%%). He no longer worries about an inbox full of emails he has to deal with at any time he login to email. He also does not have to keep any todo items in his mind because everything is recorded somewhere. However, here are some ‘pain points’ in his workflow.

*   Jim is currently using Google calendar. Because he stores/retrieves/edits todo tasks so frequently, he finds the online calendar too slow to work with. He’d rather have a desktop software he can summon quickly. Even better (but not a must) if he can activate the software by pressing a keyboard shortcut. He is quite impressed by how the [Launchy tool can be activated easily by pressing Alt+Space](http://www.launchy.net/).
*   A calendar is not very good in capturing tasks that need to be done before a specific date/time, or after a specific date/time, and items without specific times.
*   Entering an event in a calendar is a pain because it takes several clicks. He prefers a ‘one shot’ approach. e.g., to be able to type in commands such as "`add July 10, 5-6, project meeting`" (such as allowed by [GCal’s ‘quick add’ feature](http://gappstips.com/google-calendar/use-quick-add-to-speed-up-google-calendar-entries/)).
*   While it is good that all Jim’s todo items are currently online and available to access from any computer, he always uses his own laptop or office PC to access them and sometimes from places where there is no ready Internet connectivity.
*   Jim finds it a pain to do certain things important to his workflow but not so important in a regular calendar. e.g. looking for suitable slot to schedule an item, marking an item as done, deciding what todo item to do next, postponing an item.
*   A calendar does not have an easy way to “block” multiple slots when the exact timing of a task is uncertain, and release the blocked slots when the time is finalized. e.g., Block Mon 2-3pm and Tue 2-3pm for a meeting with boss → the meeting is confirmed for Tue → automatically release Mon slot.

Design your product to solve some of Jim’s problems to make his workflow even more efficient and painless. i.e. to make his life better. You don’t have to solve all problems mentioned above and there may be other problems you could solve but not mentioned above. Good software delights users by solving problems users don’t even realize they have.

**Important:** ==Command Line Interface is the primary mode of input.== The GUI is primarily for output. That is, the GUI is used to give visual feedback rather than to collect input. Some minimal use of mouse is OK (e.g. to click the minimize button), but the primary input should be command-driven. Mouse actions should have keyboard alternatives and typing is preferred over key combinations. Design the app in a way that you can do stuff faster by typing compared to mouse or key combinations.

