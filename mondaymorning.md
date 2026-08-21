### My Monday

## 9:00-9:15 - Read everything 1st and respond to nothing (Triage pass)

I skim through the items as some items might be related. After reading through the items I figured out that #2 (Niko's entity relationship refactor PR), #7 (Architecture Sync: Entity Model, same attendees), and #9 (Niko's Zod proposal) are the same workstream.I would only make sense to combine those.

## 9:15-9:35 - 1.Production Issue

Semir says "seems stable now but not sure what caused it"; This is not a closed incident yet. I will 1st go and check what was deployed recently near that specific endpoint.I will aslo confirm if Niko's PR touches risk/score and if it does carefully review it.I will then reach out to Semir and thank him for the good call then go ahead and ask him to write a post mortem / RCA on the issue.This makes sure that I am not the one debugging this; just making sure it is getting owned and documented.
Currently no customer is facing an issue so I do not perform a live debug but I make sure that the issue is not left undocumented.


## 9:35-9:45 - 8.Infrastructure Cost Question - AWS

This issue is the classic "start the clock, don't block on it" item. It is deadline drive "EOD" but not something I should fully switch to right now.I will go ahead and immediately reply with "On it, I'll have a breakdown EOD". Then I will pull the related AWS cost report or  ping  Semir ( Infrastructure & reliability,) to pull it. This issue is being actioned on in the background.

## 9:45–9:55 - 6.API documentation question — quick response before lunch 

This is quick and low-stakes but there is a real gap.I will go ahead and answer directly in a channel.Acknowledge that the API patterns have not been properly documented, direct them to what exists and the existing convention to follow for now. I also flag it as a genuine backlog item (create a ticket: "document API patterns + Bruno collection structure") rather than letting it evaporate.


## 9:55–10:15 - 5.Unhappy Client

I don't reply with a guess as that is worse than a no reply. I will start by pinging  who is responsible with building the export feature(Adona) for a real status and timeline. Then give back specifics on the issue; What is done , what is left. I own the message myself and I do not delagate cleint communications.


## 10:15-10:30 - 4.Adona's career 1:1 request

I will make sure the reply is warm, not the normal slack messages. I will set aside sometime later in the week and lock it in. I will not say "we will schedule a meeting".

## 10:30–11:00 - 2.Architecture Review  PR by Niko

This is the largest technical risk because it changes the entity model, affects twelve files and is needed for Wednesday’s pilot. I ask Niko for a concise description of the old and new models, affected workflows, database changes, backward compatibility, rollout plan and rollback plan.
I leave concrete comments before lunch. I do not wait for the 2 PM meeting to start reviewing. If the design has a fundamental problem, Niko gets that feedback early enough to adjust it.


## 11:00–11:20 - 3.Story without acceptance criteria

This is a product problem - I will send a DM to the person who owns VUL-342 (if such a person does not exist then this is a real problem to name).I will then grab Spencer for a quick 10 minute call where we will define 3 to 4 to ACs together.


## 11:20–11:35 - 9.Zod proposal

Reply to Niko and propose to move this into the 2pm architecture meeting since it touches the same code. Also let Niko keep ownership of conversation. I don't need a separate meeting for this

##  11:35–11:55 - 10.MS Graph integration

The ask contained "when you have 15-20 mins", which is a flexible ask, not urgent. But it's something I would want to give it thought.I will research what calendar sync + doc sharing via Graph would actually involve and probaly find some time over lunch to talk with Alex over this.

## 2:00–3:00- 7.Architecture meeting

I set the agenda since none existed: (1) entity relationship refactor — my PR comments, migration plan, any connection to Friday's incident, (2) Zod standardization — quick decision, Niko writes ADR, (3) confirm Kenya pilot merge timeline is realistic given open questions. This is where I engage most technically — pushing on backward compatibility and blast radius given we just had an unexplained incident in adjacent code.

## 3:00–4:30 — Compile #8 (AWS cost breakdown) and send to Finance

By now the data pull I kicked off at 9:45 is back. I actually analyze it (what changed — traffic, instance sizing, a leaked/unused resource, a bad deploy) and send Finance a real explanation, not just a number, since this is going to the CEO.


## 4:30 — Check back in on #1 and #5

Quick check: did Semir post the incident writeup, did the export-piece update land in Sumeya's update. Close the loop on both before end of day.







