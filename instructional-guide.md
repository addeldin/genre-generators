# Genre Generators Instructional Guide
## Top-Level
This activity takes place over two sequential in-class sessions. While the activity does not need to take up two full class sessions, the break is necessary so that the programs students design in groups can be implemented in code by the instructor and then shared back to the class during the next session.

The first day of the activity should take between 50 minutes and 1 hour and 25 minutes, and the second day should take between 30 and 45 minutes. I have provided estimates for how long each part of the daily activities will take, but these may need to be adjusted based on instructors' sense of what parts students will struggle with.

## Materials and Software Required
Instructors will need, at the most fundamental level:

* a computer that can run code
* the ability to project their screens to the entire class
* access to the internet to show the generator implementations
* a higher level programming language that allows for the manipulation of text strings with lists and variables (e.g. Python, which is used in `generator-template.ipynb`)
* the ability to present code and text in sequence (e.g. Jupyter Notebooks, which can present Python and Markdown in sequence, as shown in `generator-template.ipynb`)
* pen/pencils and paper for students to create collaborative documents, or a laptop for at least one student in each group to take notes to send digitally to the instructor

## Session 1

### Setup
#### Estimate: 5 to 10 minutes
To begin, tell students about the overall arc of the activity, as related in the README.

Then, introduce students to the concept of *genre* from a rhetorical perspective rather than the more colloquial use. That is, talk about written genres students are likely to encounter in class—e.g. a non-fiction personal essay, a research paper, or an argumentative essay—and distinguish this understanding of genre from the broader use that distinguishes by narrative tropes, such as science fiction, fantasy, and westerns. Whereas the former is defined by the exigence for writing based on a specific context (generally, college writing assignments) and toward a specific audience (the instructor or an imagined community relevant to the discipline, such as attendees of an academic conference), the latter tends to focus on consistent narrative tropes and structures.

Prompt students to name written genres that fit this definition. If needed, provide some examples, such as emails to your professor, obituaries, recipe blog posts, news articles, etc.

### Love Letters as a Genre
#### Estimate: 15 to 20 minutes
The setup conversations lead directly into a rhetorical analysis of the love letter genre using sample outputs from Matt Sephton's implementation of the Strachey Love Letter Generator (https://www.gingerbeardman.com/loveletter/), which is useful because it only shows generated outputs. Show students several sample letters, and ask:

* What changes for each new letter?
* What stays the same?
* What do the consistent features (e.g. a personalized salutation using a pet name) tell us about the purpose of a love letter?

Then, ask questions that consider the rhetorical dimension of love letters more broadly:

* What is a love letter?
* Why does it exist?
* When is this genre used?
* What are some key features of love letters?

### Love Letter Generation and Code
#### Estimate: 20 to 25 minutes
Once the foundations of genre, love letters, and the Love Letter Generator are established, show students Annette Vee's implementation (https://jsfiddle.net/nettework/6f7abaaa/271/), which is useful because it presents the outputs along with the underlying code. For the purposes of this activity, the HTML and CSS windows can be contracted in favor of the JavaScript and output windows.

Remind students of the consistent features they identified looking at the sample outputs of the Sephton iteration. Then, facilitate a conversation where students try to connect the word lists listed under `var` on line 4 to several outputs of the generator—e.g. how the words in `salutations1` and `salutations2` are, despite changing each time, consistently pulled from the two respective lists, which contain the opening salutation and pet name that follows it, respectively. 

While the `for` loop that starts on line 45 might be harder to mentally parse, look at the `else` statement on lines 52-54 and try to relate the combination of "YOU ARE MY", a selection from a list called `adjectives`, and a selection from a list called `nouns` is reflected in the body of the sample letters.

Cap off this part of the activity by emphasizing the essential tools used to generate new love letters: text strings, lists of words that can be chosen from at random and inserted into a text string, and the use of variables in text strings to create differences between sample outputs.

### Group Programming Exercise
#### Estimate: 20 to 30 minutes
Break students into groups of between 4 and 6 students. If a subset of the class has experience with computer programming, distribute them evenly amongst the groups, as they might be able to guide how students enact their ideas into a conceptual program.

Ask them to respond to the following prompts in a collaborative written document and either turn in the paper or send their document to the instructor digitally at the end of class.

1. Identify a written genre.
2. Why does this genre exist? When is it used?
3. What are the key features of the genre?
4. What key features might be easy to encode? What might be difficult?
5. Create a mix of text templates, variables, and lists that could generate new instances of this genre based on the features you have identified.

Emphasize that you will enact a selection of the student programs in code to present for the next class.

## Between Sessions

Identify 1 or 2 student programs that seem particularly viable to represent in code. For example, broadly described generator programs that do not contain lists or templates that interact with variables will require more labor on the part of the instructor to translate that program into code. While there are many potential approaches students can take, an ideal program for this activity will provide a basic string template, a list of words that is chosen from for parts of the template, and potentially variables that are called (e.g. the current time of day using the `datetime` module in Python).

Present text from the student document that states the chosen genre, the students who designed the generator, the description of that genre, and the key features they identified. Then, demonstrate the code that enacts the program with comments that explain what a given section is doing. The code should be presented in software that can run the code and present outputs along with the code, so that the generator can be run repeatedly to look at several different outputs.

For the materials included in this repository, I used Jupyter Notebooks to present text in Markdown in sequence with actionable code in Python. Please see `student-generator.ipynb` for an example, or `generator-template.ipynb` for a notebook that can be easily added to for instructors trying this activity.

## Session 2

### Setup
#### Estimate: 5 minutes
Briefly summarize the activity of the previous session, in particular for students who may have been absent.

### Process Reflection
#### Estimate: 5 to 10 minutes
Ask students the following questions to encourage them to reflect on their processes:

* How did your group take your genre and design a generator for it?
* How did you consider the role of the computer as you designed?
* What did you leave out of your generator that is part of the genre you described? Why?
* Would you call what your group did *programming*?

I used the final question as an opportunity to reinforce the broader idea behind the activity: programming is a conceptual process that mediates human goals and representations of the world and the digital technology that works with these representations in code. While their decisions had to account for the technical elements of digital technology, they were still making decisions about what a genre is, who it's for, when it's used, and what elements define it. They programmed by considering how to take their goals in defining a genre to generate new examples and make them work in the logic of digital technology. While the instructor does the actual coding, which is itself mediational, the focus is on how the students mediated human understanding and digital representation.

### Genre Generator Presentation
#### Estimate: 15 to 20 minutes
Show students the formatted text and code. Read through the name of the genre students chose, the names of the students who designed the generator, their description of the genre, and the key features they identified.

Relate a key feature to the code, which can generally be broken up for readability similar to the Vee implementation of the Love Letter Generator. For example, have all of the lists of terms in sequence, then the variables that choose from the lists, then the string template that makes use of the variables. If students identified that a salutation was important for an email to a professor, for example, then relate this key feature to the lists, variables, and place in the template that generate the salutation specifically.

Show several sample outputs of the generator and ask students to identify which key features they can see in the outputs, and try to relate those outputs to what they can see in the code.

### Rhetorical Analysis of the Genre
#### Estimate: 10 to 15 minutes
Guide students through a rhetorical analysis of the genre as a mirror of the session 1 discussion on love letters. You might ask about a number of specific features in the generator, but these general questions that are useful starting points are:

* What does this generator tell us about this genre?
* Why does this genre exist, and what does it do?
* How does this generator reflect these aspects of the genre?
* What aspects of the genre are important that you do not see included here? Why might they not be there?

The final question I like to ask to reiterate the sociotechnical nature of the genre generators is:

* Do these generators objectively identify what their respective genres *are*, or their key features?

Emphasize that, while the relatively objective functioning of the machine does produce consistent outputs based on the rules defined in the code, they no less are built on subjective decisions about what the genre is and how to represent it. As a result, *programming* is not an inherently objective means of representing the world, but one that mediates the world in consideration of technological limitations and affordances.