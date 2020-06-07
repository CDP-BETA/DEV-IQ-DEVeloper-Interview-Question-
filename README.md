# DEV-IQ(DEVeloper Interview Question)


Go to Challenge 👉
여기 이나이즈 버튼 와야함

## 💯 A simple online python quiz
- Levels are set based on the quiz score
- Solve quiz and check your level (please don't take it too seriously)!

## ⌨️ How to use
- Open web browser(recommend `Chrome` browser)
- Connect `http://localhost:3000`(It's for local environment. other uses `http://<IP>:<PORT>` form)
- Click `Start a Quiz`
- Enjoy quiz!
- You can see the score and the correct answers
- Share the result with your friends 

## 🚀 How to run

### On local(dev)
```
npm install -g nodemon
npm install
npm run watch
npm run dev
```
### On local(prod)
```
npm install
npm run build
npm run production
```

### Thru docker
```
docker build -t <Name> .
docker run -p 80:3000 -d <Name>
```

## 🛠 How to contribute
Feel free to post issues and send pull requests. We need more items in the quiz pool!

### Basic contribution Guidelines
Ensure your pull request adheres to the following guidelines.
- Create issues if you have any interesting ideas or bug reports
- Use English in all cases (communication, comment, and code review etc)

### Code contribution guide
- Indentation of 4 spaces
- For React component file names, use pascal case. For other cases, use snake case.
- For React component variable names, use pascal case. For other cases, use camel case.
- Refer to existing code if you are not sure

### Quiz pool contribution guide
- Sync answers with questions
- Questions and answers are managed in JSON format. See the examples below:
  - Question ([/src/static/json/python.json](https://github.com/ainize-team/python-level-challenge/blob/master/src/static/json/python.json))
    ```
    {
        "Id": (Integer, problem number in ascending order)[Required],
        "Subject": (String)[Required],
        "Difficulty": (Integer, 0:Easy 1:Normal 2:Hard)[Required],
        "Question": (String)[Required],
        "Code": (String)[Optional],
        "Answers": (Array of String)[Required],
        "Reference": (String)[Optional]
    }
    ```
  - Answer ([/src/static/json/python_answer.json](https://github.com/ainize-team/python-level-challenge/blob/master/src/static/json/python_answer.json))
    ```
    {
        "Id": (Integer, answer number in ascending order, must sync with question number)
        "Answer": (Integer, 0 ~ ...)
    }
    ```

## Notice
For developer interview quiz pool pool generation, we referred to the following web-sites.
- https://github.com/gyoogle/tech-interview-for-developer
- https://github.com/JaeYeopHan/Interview_Question_for_Beginner
