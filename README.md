# MoodWave: An Emotion-Based Music Recommendation System

## Proposal Report

### 動機與目標
In many music applications, listening is treated as a relatively static activity—users select a playlist, and the system continues playing songs without adapting to changes in the user’s state. However, in real life, human emotions are dynamic, multi-layered, and constantly evolving. A person may feel calm, sad, and relaxed at the same time, and these emotions can shift significantly within a short period.

Another challenge is that music recommendation is inherently subjective. Even if a system attempts to match a user’s mood, the recommended song may not always meet the user’s expectations. This creates a need for systems that can not only generate recommendations, but also adapt based on user feedback.

This project is motivated by the idea that music recommendation should be responsive, adaptive, and interactive. Instead of asking “which playlist do you want?”, the system focuses on understanding “how you feel right now” and adjusting its suggestions accordingly.

The goal of this project is to design a simple command-line (CLI) music recommendation system that dynamically adapts to the user’s mood, activity, and energy level. The system also incorporates basic feedback mechanisms (such as like/skip) to refine recommendations within a session.

Through this project, I aim to explore how abstract human emotions can be transformed into computable values using data structures and algorithmic logic, while also handling the uncertainty and subjectivity of user preferences.

### 預期功能
- User inputs current mood (single or multiple) 
- User selects current activity (e.g., studying, resting)
- User inputs energy level (1–5)
- System reads and evaluates song data
- Calculates a matching score for each song (scoring algorithm)
- Recommends the most suitable songs
- Displays top-ranked results (ranking)
- User can like or skip songs
- Maintains a simple recommendation history
- System prompts the user to update their mood after some interactions
- When the mood changes, the system regenerates recommendations accordingly


### 使用技術
- Programming Language: Python 3
- Interface: Command Line Interface (CLI)
- Data Storage: JSON files (for song data and user history, no external database required), as the system primarily relies on iterating through all songs for scoring rather than complex queries, making a lightweight structure sufficient for the project.
- Libraries: Built-in Python libraries (e.g., `json`, `random`)
- Programming Approach: Object-Oriented Programming (OOP) and basic algorithm design (linear search and scoring mechanism)


### 時程規劃

- Week 7 — Proposal
  Finalize the project idea, complete the proposal report, and design the data format for songs, user input, and recommendation history.

- Week 8 — Data and Structure Design
  Implement the `Song` class, prepare an initial song dataset, and set up JSON-based data loading and saving.

- Week 9 — Recommendation Logic
  Design and implement the weighted scoring algorithm for mood, activity, and energy matching. Test the logic with sample inputs.

- Week 10 — Core User Flow 
  Implement the main CLI flow, including user input, score calculation, ranking, and recommendation display.

- Week 11 — Prototype
  Add like/skip feedback, recommendation history, and mood update prompts. Complete the prototype report.

- Week 12 — Refinement 
  Improve the scoring formula, expand the dataset, and refine the recommendation criteria.

- Week 13 — History and Adaptation 
  Improve history handling and use user feedback to adjust recommendations within a session.

- Week 14 — Testing and Polish
  Conduct end-to-end testing, fix bugs, and improve code structure and CLI output formatting.

- Week 15 — Final Submission 
  Finalize the system, complete the final report, and record the demo video.

### 與課程的關聯
This project involves several fundamental data structures and algorithmic concepts, chosen based on how well they fit the problem.
A **list** is used to store the song library, as the system evaluates each song sequentially during scoring. This makes iteration simple and efficient.
A **dictionary (hash map)** may be used to map activities to song attributes, allowing efficient lookups without scanning the entire dataset.
The core of the system is a **weighted scoring algorithm**: score = (mood_match × 3) + (activity_match × 2) + (energy_match × 1)
This algorithm converts subjective user input (such as emotions) into numerical values that can be compared and ranked.
The system also uses **linear search** to evaluate each song and **sorting** to rank songs by relevance, ensuring that the most suitable recommendations are selected.
These choices allow the system to efficiently organize data, process user input, and generate meaningful recommendations.

### Evaluation of the System

| Criteria | Success Condition |
|---|---|
| **Scoring correctness** | Given the same input, the system should always produce the same ranked output. A song with fully matching mood, activity, and energy should score higher than a song with no match. |
| **Recommendation quality** | At least 2 of the top 3 recommended songs should directly overlap with the user’s input mood tags or activity context. |
| **Feature completeness** | All core features should work end-to-end: input → scoring → ranking → display → like/skip → history → mood update → re-recommendation. |
| **Data persistence** | After closing and restarting the program, recommendation history and liked songs should be restored correctly from the JSON file. |
| **Mood update flow** | After the user updates their mood, the new recommendations should differ from the previous ones and better match the updated mood tags. |
| **Edge case handling** | If the user enters an unrecognized mood or leaves a field blank, the system should show a clear prompt instead of crashing. |

## Prototype Report

### 目前進度
<!-- 完成了什麼 -->

### 遇到的困難
<!-- 遇到什麼問題、如何解決或打算如何解決 -->

### 下一步計畫
<!-- 接下來要做什麼 -->

### 與課程的關聯
<!-- 到目前為止，你的實作中哪些部分與課程內容有關？關係是什麼？ -->

---

## Final Report

### 專案說明
<!-- 完整描述你的專案做了什麼 -->

### 使用方式
<!-- 如何編譯、執行、使用你的程式 -->

### 與課程的關聯總結
<!-- 總結你的專題與進階程式設計及資料結構課程之間的關聯 -->
