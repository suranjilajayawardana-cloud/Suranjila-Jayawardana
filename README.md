# An AI Recycling Guide
Group 22
SortSmart: An AI Recycling Guide
Project proposal
Group members: Suranjila Jayawardana and Madhuni Kanchana
Project idea
People sometimes find it difficult to decide where an item should be disposed of. Packaging can contain several materials, and a general answer may not match local sorting instructions. Our group plans to build SortSmart, a simple web application that helps users identify a suitable waste category from a written description of an item. The application will explain its suggestion and remind users to follow the waste collection rules for their own municipality.
Who is it for?
The intended users are students, households, and people new to the local recycling system. The first version will use a small, clearly identified set of example sorting rules and will be a learning prototype. It will not claim to provide authoritative guidance for every location or item.
Main features
1. A user types an item, such as “empty plastic yoghurt cup” or “used paper towel.”
2. The app suggests a waste category and shows a short explanation.
3. The app asks for a relevant detail when the description is unclear, for example whether a package is empty.
4. The user can view the source or rule behind the suggestion and report that an answer seems incorrect.
5. If the app cannot determine a suitable category, it says so and directs the user to check their local waste provider's instructions.
The initial prototype will handle a limited set of common household items and categories, such as paper, cardboard, plastic packaging, glass packaging, metal, biowaste, mixed waste, and items needing a separate collection point. We will document exactly which cases the prototype covers.
AI component
We will build a text classification component that maps a user's item description to candidate waste categories. We will compare it with a simple keyword-based baseline. The app will display a category only when its result is sufficiently supported by the example rules; otherwise it will ask a clarification question or show an uncertain result. The explanation will refer to the relevant material or condition rather than inventing a rule.
We will test the classifier on descriptions that differ from its training examples, including ambiguous and multi-material items. We will report where it makes mistakes. The exact model may be adjusted after early experiments to keep the project feasible for two students.
Data and responsible use
We will create a small labelled dataset of example item descriptions and categories. Before using any real sorting rule, we will check the instructions of a named local waste provider and record the source, location, and access date in the repository. We will not copy large amounts of source text or present a general Finnish rule as if it applies everywhere. The prototype does not require personal data, user accounts, or photographs.
Planned tools
- Python for the application logic and data processing.
- Streamlit for a simple web interface.
- pandas and scikit-learn to manage examples and test a text classifier.
- CSV or JSON to store labelled examples and the limited set of documented rules.
- GitHub for shared development using the course starter template.
These tools are our initial plan; we may simplify the implementation if testing shows a smaller approach works better.
Two-person work plan
Stage	Suranjila	Second group member
Plan	Define users, example items, and interface requirements	Define categories, data format, and technical approach
Build	Create the Streamlit input, results, and feedback screens	Prepare labelled examples and implement the classifier and baseline
Test	Test whether explanations are clear and questions are useful	Measure classification results and investigate incorrect predictions
Document	Write the user guide and project reflection	Write setup instructions and technical evaluation


We will review and integrate each other's work. Each member will use their own GitHub account, make regular commits, and push their own contributions to the one shared group repository. Commit messages will describe the changes, for example Add recycling item form or Evaluate text classifier.
Evaluation and expected result
We will test the app with a separate set of item descriptions and compare the AI classifier with the keyword baseline. We will check whether the displayed category matches the documented rule, whether uncertain cases are handled honestly, and whether a new user understands the explanation. The final result will be a working prototype, labelled sample data, setup instructions, and a short report on accuracy and limitations.
Scope
For this course project we aim to make a usable prototype for a limited set of common items, not a complete national recycling service. The app will not identify items from images or determine rules automatically from the user's location. Any later expansion would need more verified local rules and further testing.
