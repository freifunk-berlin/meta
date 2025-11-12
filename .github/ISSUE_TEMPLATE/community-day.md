---
name: Community day planing
about: Template for the planing of the next community day
title: 'Community day <Year>'
labels: ''
assignees: ''

---

**📍 Location:** _undecided_
**📅 Date:** _undecided_
**💬 Topics:** _undecided_

## Preparation

### Phase 1 (-5W)
- [ ] Agree on a date
- [ ] Collect topics
- [ ] Agree on topics

<details>
<summary>📄 Instructions and templates</summary>
<details>
<summary>Coordinate dates and collect topics</summary>

**Matrix**
```md
## CommunityDay <Season> <Year> Planung

**[DE]** Die Planung für den nächsten Community Day hat begonnen. Wer mithelfen will fügt sich bitte selbst zu dem verlinkten Issue hinzu. Als erstes müssen wir klären welcher Tag am besten passt. Hier die Abstimmung dazu. In Kürze kommt die Abstimmung zu den Themen für das Treffen. Bitte legt ein [Need for discussion](https://github.com/freifunk-berlin/meta/issues?q=state%3Aopen%20label%3A%22Need%20for%20discussion%22) Issue an, wenn ihr ein weiteres Thema vorschlagen wollt.

**[EN]** The planing for the next Community Day has started. If you would like to help, please assign yourself to the linked issue. First, we need to decide which day works best. Here is the poll. The vote on the topics for the meeting will take place shortly. Please create a [Need for discussion](https://github.com/freifunk-berlin/meta/issues?q=state%3Aopen%20label%3A%22Need%20for%20discussion%22) issue if you would like to suggest another topic.

- Issue: <Issue>
- Deadline: <Deadline>
```

</details>
<details>
<summary>Agree on topics</summary>

**Matrix**
```md
## CommunityDay <Season> <Year> topic selection

**[DE]** Damit wir den Community Day gut vorbereiten und keine Themen untergehen, gibt es hier eine Abstimmung zu den Themen. Bitte gebt an, welche Themen ihr gerade wichtig findet für das nächste Treffen.

**[EN]**  To help us prepare for Community Day and ensure that no topics are overlooked, we are holding a vote on the topics here. Please indicate which topics you think are important for the next meeting.

Issue: <Issue>
Deadline: <Deadline>
```

```Python
# Minimalistic python script to get issues as md for copy paste into matrix poll.
import requests
response = requests.get(
    "https://api.github.com/repos/freifunk-berlin/meta/issues",
    params={"state": "open", "labels": "need for discussion"},
)
for issue in response.json():
    print(f"[{issue['title']}]({issue['html_url']})\n")
```
</details>
</details>

### Phase 2 (-4W)
- [ ] Find people for the topics
- [ ] Reduce topics to a realistic level
- [ ] Enter in the calendar
- [ ] Send invitations
- [ ] Book a room
- [ ] Find a moderator

<details>
<summary>📄 Instructions and templates</summary>
<details>
<summary>Calendar entry</summary>

[Instructions for creating an appointment](https://github.com/freifunk-berlin/berlin.freifunk.net?tab=readme-ov-file#events)

**EN**

```md
On Community Day, we come together to discuss important topics related to the Berlin Freifunk network. On this day, we take the time to discuss larger issues that cannot be easily resolved via chat. Between the reviews and previews, there will be hot food and snacks. To facilitate discussion of the topics, the preparation group has drawn up an [agenda with a schedule](<Issue>). Afterwards, there will be plenty of time for informal discussion.
```

**DE**

```md
Am Communityday kommen wir zusammen, um uns über wichtige Themen im Berliner Freifunk-Netz auszutauschen. An diesem Tag nehmen wir uns Zeit, um auch größere Themen zu besprechen, die sich nicht einfach per Chat lösen lassen. Zwischen den Rück- und Ausblicken gibt es warmes Essen und Snacks. Um die Themen gut besprechen zu können, hat die Vorbereitungsgruppe eine [Agenda mit Zeitplan](<Issue>) aufgestellt. Im Anschluss bleibt noch genügend Zeit für einen lockeren Austausch.
```

</details>

<details>
<summary>Invitation</summary>

**Mail**
[Create email to mailing list](mailto:berlin@berlin.freifunk.net?subject=CommunityDay%20%3CJahreszeit%3E%20%3CJahr%3E%20%3CDatum%3E&body=%F0%9F%93%8D%20Locations%3A%20%3COrt%3E%0A%F0%9F%93%85%20Date%3A%20%3CDatum%3E%20%3CZeit%3E%0A%F0%9F%92%AC%20Agenda%3A%20%3CIssue%3E%0A%0A%5BDE%5D%0AAm%20Communityday%20kommen%20wir%20zusammen%2C%20um%20uns%20%C3%BCber%20wichtige%20Themen%20im%20Berliner%20Freifunk-Netz%20auszutauschen.%20An%20diesem%20Tag%20nehmen%20wir%20uns%20Zeit%2C%20um%20auch%20gr%C3%B6%C3%9Fere%20Themen%20zu%20besprechen%2C%20die%20sich%20nicht%20einfach%20per%20Chat%20l%C3%B6sen%20lassen.%20Zwischen%20den%20R%C3%BCck-%20und%20Ausblicken%20gibt%20es%20warmes%20Essen%20und%20Snacks.%20Um%20die%20Themen%20gut%20besprechen%20zu%20k%C3%B6nnen%2C%20hat%20die%20Vorbereitungsgruppe%20eine%20%5BAgenda%20mit%20Zeitplan%5D(%3CIssue%3E)%20aufgestellt.%20Im%20Anschluss%20bleibt%20noch%20gen%C3%BCgend%20Zeit%20f%C3%BCr%20einen%20lockeren%20Austausch.%0A%0A%5BEN%5D%0AOn%20Community%20Day%2C%20we%20come%20together%20to%20discuss%20important%20topics%20related%20to%20the%20Berlin%20Freifunk%20network.%20On%20this%20day%2C%20we%20take%20the%20time%20to%20discuss%20larger%20issues%20that%20cannot%20be%20easily%20resolved%20via%20chat.%20Between%20the%20reviews%20and%20previews%2C%20there%20will%20be%20hot%20food%20and%20snacks.%20To%20facilitate%20discussion%20of%20the%20topics%2C%20the%20preparation%20group%20has%20drawn%20up%20an%20%5Bagenda%20with%20a%20schedule%5D(%3CIssue%3E).%20Afterwards%2C%20there%20will%20be%20plenty%20of%20time%20for%20informal%20discussion.)

**Matrix**

```md
## CommunityDay <Season> <Year> <Date>

**📍 Location:** <Ort>
**📅 Date:** <Datum> <Zeit>
**💬 Agenda:** <Issue>

### [DE]
Am Communityday kommen wir zusammen, um uns über wichtige Themen im Berliner Freifunk-Netz auszutauschen. An diesem Tag nehmen wir uns Zeit, um auch größere Themen zu besprechen, die sich nicht einfach per Chat lösen lassen. Zwischen den Rück- und Ausblicken gibt es warmes Essen und Snacks. Um die Themen gut besprechen zu können, hat die Vorbereitungsgruppe eine [Agenda mit Zeitplan](<Issue>) aufgestellt. Im Anschluss bleibt noch genügend Zeit für einen lockeren Austausch.

### [EN]
On Community Day, we come together to discuss important topics related to the Berlin Freifunk network. On this day, we take the time to discuss larger issues that cannot be easily resolved via chat. Between the reviews and previews, there will be hot food and snacks. To facilitate discussion of the topics, the preparation group has drawn up an [agenda with a schedule](<Issue>). Afterwards, there will be plenty of time for informal discussion.
```

</details>
<details>
<summary>Moderation</summary>

## How to Moderation

## Moderation Guide

Moderation is not as difficult as we sometimes think. Nevertheless, it is important to keep a few points in mind, not only to ensure respectful interaction, but also to make our community days productive.

## Moderation tasks:

**Social**
- Make sure that everyone feels comfortable in conversations.
- Keep an eye on the speaking times of those involved.
- Let everyone have their say. If necessary, address quieter people directly.
- Involve new members of the community. Allow space for questions and offer brief explanations.
- Pay attention to the needs of the group. Is it time for a break or an energizer?

**General**
- Maintain an overview.
- Respond to questions.
- Allow different points of view to be expressed in discussions and avoid unnecessary repetition.
- Record the results again after discussions.
- Choose the right moderation techniques for the various agenda items.

**Community Day Schedule**
- Start the meeting (welcome, introductions).
- Assign tasks (minutes, keep an eye on the time).
- Present the agenda and goals for the day.
- After breaks, bring the group back together/call for quiet.
- Enable a quick re-entry. (What did we do before the break, what happens next?)
- At the end of the day, briefly review the goals and results and take stock.
- Say goodbye, give another opportunity for feedback, and mention the next community event. 

</details>

<details>
<summary>Location</summary>

[List of possible rooms](https://wiki.freifunk.net/Berlin:Treffen)

</details>
</details>

### Phase 3 (-2W)
- [ ] Send reminder
- [ ] Plan food

<details>
<summary>📄 Instructions and templates</summary>
<details>
<summary>Reminder</summary>

**Matrix**

```md
**⏰ Reminder: CommunityDay<Season> <Year> <Date>**

- 📍 Locations: <Ort>
- 📅 Date: <Datum> <Zeit>
- 💬 Agenda: <Issue>
```

</details>
<details>
<summary>Verpflegung abfrage</summary>

**Matrix**

```md
**🥙 CommunityDay<Season> <Year> <Date>**

[DE] Wir brauchen noch Personen die sich um das Essen am CommunityDay kümmern können. Wer kann sich vorstellen dafür Verantwortung zu übernehmen?

[EN] We still need people who can take care of the food on Community Day. Who would be willing to take on this responsibility?
```

</details>
</details>

### Phase 4 (-3T)
- [ ] Send reminder
- [ ] Get the food

<details>
<summary>📄 Instructions and templates</summary>

**Matrix**

```md
**⏰ Reminder: CommunityDay<Season> <Year> <Date>**

- 📍 Locations: <Ort>
- 📅 Date: <Datum> <Zeit>
- 💬 Agenda: <Issue>
```

</details>

### Phase 5 (+1W)
- [ ] Protokoll abspeichern
- [ ] Protokoll verschicken
- [ ] Issue schließen

<details>
<summary>📄 Instructions and templates</summary>

[Upload o the minutes](https://github.com/freifunk-berlin/meta/blob/main/protokolle/)

</details>

## Schedule

1. Arrival _(20 min)_
2. Introduction to the schedule _(10 min)_
3. Welcome round, motivation, and frustrations _(30 min)_
4. State of the Network _(30 min)_
5. Maintenance _(20 min)_
6. Topics Block 1 _(60 min+)_
7. Break with food _(40 min)_
8. Topics Block 2 _(60 min+)_
9. Joint conclusion _(10 min)_
