# Realtime Kanban Board

React JS - Senior Technical Assessment

## IMPORTANT

1. For this task, you need to create a React application, while also utilizing any third party libraries that you feel will help you complete the task efficiently. Try to minimize the usage of these third party libraries and only use the most necessary ones that you feel will help you get the job done.

2. Don't be afraid to research (Google, LLMs etc) for potential/partial solutions to specific things that you may get stuck on. The point is not for you to be able to create such layouts from scratch by heart, but rather **to be able to research, learn and understand the problems as well as their solutions**. \
   As long as you manage to solve the tasks at hand, while having a deep understanding on how and why they were implemented the way that they were - you will have done a great job.

## The challenge

Your challenge is to build out a Real-time personal Kanban board.

> Note: Desktop only layout is needed. No need to focus on responsive design. Can just show a message saying something like "Please use the desktop version of <_app name here_>"

As a user, you should be able to:

1. Create your own access to the board (similar to signing in), by entering your name/email/username when firstly accessing the app

- This needs to essentially function as a very simple auth system:
  - Your choice on if users register with name/email/username (however, this needs to be unique among users, proper error handling is required if name/email/username is not unique)
  - No password needed for the purposes of the task
  - They can then sign-out using a simple sign-out button
- Don't worry about the security aspect - the main purpose for this is to keep a single user entity connected to their Kanban board data
- How you choose to store this auth information is up to you, however try to keep in mind the pros and cons of your choice

2. Create/Rename/Delete Columns for the board (ex. "Backlog", "In Progress", "Ready for Testing" etc.)

   - The column's order should be able to be changed by the user (you can choose to do this via a Drag n' Drop functionality or just simple buttons that change the order)

3. Create/Remove tickets. Each ticket should have:
   - Title (mustn't be an empty string)
   - Description (mustn't be larger than 1024 characters)
   - Status (Representing the column it is currently in)
   - Tags (string values that can be dynamically created with each ticket)
     - The created tags need to persist and be given as autocomplete options for future tickets
     - Deleting a ticket does NOT delete the tag entity associated with it, meaning the tag previously associated with the ticket should still be present as an autocomplete option for future tickets. For the purposes of this task, the number of tags can theoretically increase infinitely
     - Optionally, can associate a color with each tag (either random color at tag creation, or a color picker when creating the tag)

- A ticket shown on the board's columns, should show its information as such:
  - The title needs to be restricted to a maximum of 1 line of text. More than that and there needs to be an ellipsis (...) cutting the text off
  - The description needs to be restricted to a maximum of 3 lines of text. More than that and there needs to be an ellipsis (...) cutting the text off
  - The tags need to be shown as a horizontally-spanning list of a maximum of 3 items. More than that and there needs to be a small UI indicator (number) of the remaining number of tags
    Ex. If there are 5 tags associated with the ticket - show the first 3 and show a "+2" indicator next to them
  - The Status doesn't need to be shown in this view, as the column it is in - represents the Status value
- Clicking on a ticket should open up a modal showing its full details, where the full title, description, tags list and status are shown, along with a button that can delete the ticket
- The tickets should not be editable (apart from their Status obviously). You can only create them, remove them or move them to a different column
- Moving the tickets to different column can either be done using Drag n' Drop functionality or just simple dropdown that changes the status (a.k.a. column) of the ticket

4. Filter the tickets shown on the board based on their tags (multi value select input)

- This filtering needs to be reflected in the URL of the page and opening the page with such a URL should automatically filter the tickets accordingly

5. **The Kanban board needs to show its state in real-time**. This means that if you "sign in" from 2 different browsers - **changing a ticket's status should be reflected in both browsers at the same time**.

- Only the ticket's status changing should be reflected in real time. Any other changes like creating/deleting a column or a ticket don't need to be shown in real-time (but they may arise as a natural progression of the real-time ticket status change, depending on the implementation 😉)

---

You need to choose the appropriate database(s) for storing such information - both the persistent and the real-time data.

> Note: If the real-time functionality is not implemented, this task can still theoretically be passed, provided that the rest of the functionality is done correctly and during the following one-on-one discussion, you can provide a reasonable theoretical explanation on how you might go about implementing such a feature.

## Style guidelines

- There are no strict guidelines on how the app should look like. However, the design should at least be reasonably clean and understandable, easily usable and ideally accessible

- Don't be afraid to use any third party libraries that you may need for crucial things such as basic UI components like modals, form inputs etc (although you can feel free to create them on your own), async state management, database communication etc

- The main idea is that you understand the basic way that these third party tools work and HOW they help you in your goal. Don't use them as a crutch but rather as a helpful tool and try to understand how they provide that help
- It is vital that you take your time to choose the best tools for the job at hand. This includes the state management approaches, the storage solutions, the data structure etc.

## Submitting the solution

Feel free to either create a GitHub or a GitLab repo and add me as a member of the project:

- [My GitHub profile](https://github.com/dshijakovskiTDL)
- [My GitLab profile](https://code.tdlbox.com/daniel.shijakovski)

After submission, feel free to ping me on Discord - I will review the task and schedule a subsequent one-on-one call where we will discuss the solution, your approaches to solving the task etc. After that, if all goes well, the assessment will be considered as passed.

If there are any questions, don't hesitate to write in the Discord chat, will do my best to answer any unclear topics.

Good luck and crush it! 💪
