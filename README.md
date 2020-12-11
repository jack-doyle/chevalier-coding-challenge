# Intro

**Please build an app that allows a user to answer questions for a claim check.**

This exercise requires a little bit of frontend and/or backend.

If you're stronger on the backend, that's fine to concentrate on that more - just let us know in the notes you've done so (and likewise for the front end).
Please, however, ensure both the client and/or server side is _well tested_ and _clean code_ and that the code works before you submit it.

Please also include a short README, with instructions on how to run/access the project.

## Claim check

A claim check is a set of questions that a potential customer can answer about their current case/situation. Upon completing the claim check's questions, the user is presented with a final view.

A claim check may be dynamic; the next question for a user might depend on the answer to the current question, or on the combination of answers to previous questions. For this, you might think about a way to store answers to questions, in order to retrieve them later on.

A claim check may have multiple final states. These are states where there are no more questions for the user, however the user is given the option to reset the claim check and return to the first question.

You can have a look at [Chevalier's claim check here](https://check.kanzlei-chevalier.de/kuendigung).

### Client side
Requirements:
- Please ensure it can be used on multiple screen sizes
- Every question should have its separate page or UI state

It's completely up to you what frameworks you use; we use react for web, and all the common libraries that allows modern frontends and easier testing. Additionally, feel free to design it however you like.

### Server side
The server side can be in whatever language you are strong with. We mainly use Javascript, Java or Python, so please try to use one of them that you're stronger with.

There is a [small JSON file provided](./claim-check.json) that contains all of the questions for the claim check. Please use this data as the basis for your service. You can see an overview of the question flow below.

Optional: If you opt to use a database, please import this data as your starting point, and ensure you provide full setup script or instructions for the database.
You can use whatever storage you think fits the problem.

### Flow
[![](https://mermaid.ink/img/eyJjb2RlIjoic3RhdGVEaWFncmFtLXYyXG4gICAgWypdIC0tPiBESVNNSVNTQUxfUkVDRUlWRURcbiAgICBESVNNSVNTQUxfUkVDRUlWRUQgLS0-IFlFU1xuICAgIERJU01JU1NBTF9SRUNFSVZFRCAtLT4gTk9cbiAgICBZRVMgLS0-IE5VTUJFUl9FTVBMT1lFRVNcbiAgICBOTyAtLT4gRVhJVFxuICAgIE5VTUJFUl9FTVBMT1lFRVMgLS0-IE9WRVJfVEVOX0VNUExPWUVFU1xuICAgIE5VTUJFUl9FTVBMT1lFRVMgLS0-IFVOREVSX1RFTl9FTVBMT1lFRVNcbiAgICBPVkVSX1RFTl9FTVBMT1lFRVMgLS0-IFNVQ0NFU1NcbiAgICBVTkRFUl9URU5fRU1QTE9ZRUVTIC0tPiBFWElUXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoic3RhdGVEaWFncmFtLXYyXG4gICAgWypdIC0tPiBESVNNSVNTQUxfUkVDRUlWRURcbiAgICBESVNNSVNTQUxfUkVDRUlWRUQgLS0-IFlFU1xuICAgIERJU01JU1NBTF9SRUNFSVZFRCAtLT4gTk9cbiAgICBZRVMgLS0-IE5VTUJFUl9FTVBMT1lFRVNcbiAgICBOTyAtLT4gRVhJVFxuICAgIE5VTUJFUl9FTVBMT1lFRVMgLS0-IE9WRVJfVEVOX0VNUExPWUVFU1xuICAgIE5VTUJFUl9FTVBMT1lFRVMgLS0-IFVOREVSX1RFTl9FTVBMT1lFRVNcbiAgICBPVkVSX1RFTl9FTVBMT1lFRVMgLS0-IFNVQ0NFU1NcbiAgICBVTkRFUl9URU5fRU1QTE9ZRUVTIC0tPiBFWElUXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)

### Acceptance criteria
- The claim check questions should be answerable
- Each point in the above flow should be reachable by answering the questions
- It should be possible to reset the claim check after reaching a final state
- It should be possible to go back to a previous question in the claim check
