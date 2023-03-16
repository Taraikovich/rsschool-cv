# Igor Taraikovich

*Beginner frontend developer. I am a fast learner. I have experience in creating simple sites for small businesses. I want to work on big serious projects in the team.*

> ### Contact Information:
- **phone:** +995 59 318 19 53
- **email:** taraikovich@outlook.com
- **telegram**: @Taraikovich

[========]

### Skills:
- HTML
- CSS
- JavaScript
- Angular (*in the process of studyin*g)
- Git

[========]
### Sample JavaScript code:
```javascript
let list = document.querySelector('.list');
let rand = document.querySelector('.random');
let input = document.getElementById("input-id");
let load = document.querySelector('.load');
let arr = [];
let loadArr = [' |-- loading', ' -|- loading', ' --| loading'];

input.addEventListener('keyup', (e) => {
    if (e.code === 'Enter' || e.code === 'NumpadEnter') {
        if (arr.length >= 1) rand.hidden = false;
        list.children[1].innerHTML += `<tr><td>"${document.getElementById("input-id").value}"</td><td>-</td><td>0</td></tr>`;
        document.getElementById("input-id").value = '';
        arr.push(0);
    };
});

function randomNumber() {
    return Math.floor(Math.random() * arr.length);
};

function graficalPecents(x) {
    let a = '';
    for (i = 1; i <= x; i++) a += '|';
    return x + '% ' + a;
}

rand.addEventListener('click', () => {

    rand.hidden = true;
    input.hidden = true;

    let timer = setInterval(() => {
        arr[randomNumber()] += 1;
        let percents = [];
        arr.forEach(element => {
            percents.push(graficalPecents(Math.floor(100 / arr.reduce((a, i) => a + i) * element)));
        });
        for (let i = 0; i < arr.length; i++) {
            list.children[1].children[i].children[2].textContent = `${percents[i]}`;
        };
        
        if (load.textContent === loadArr[0]) {
            load.textContent = loadArr[1];
        } else if (load.textContent === loadArr[1]) {
            load.textContent = loadArr[2];
        } else {
            load.textContent = loadArr[0];
        };
    }, 100);

    setTimeout(() => { clearInterval(timer); load.textContent = 'Finish!!!'; }, 10000);

});
```

[========]
### My projects:
|![](https://github.com/Taraikovich/assets/blob/main/CSSBAYAN.png?raw=true)  | CSSBayan [link](https://taraikovich.github.io/cssBayan/cssBayan/index.html "link")  |
| ------------ | ------------ |
|  ![](https://github.com/Taraikovich/assets/blob/main/FakeVote.png?raw=true) | **FakeVote** [**link**](https://idyllic-pastelito-86f455.netlify.app/ "link") |

[========]

### Education:
- **RS School** (December 5, 2022 - ...)

[========]

### English level:
- **B1** (Intermediate)

