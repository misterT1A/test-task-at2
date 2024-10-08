## Инкапсуляция, наследование и полиморфизм — это три ключевые концепции объектно-ориентированного программирования (ООП)
* ### Инкапсуляция
   это когда мы скрываем детали реализации от посторонних, делая переменные и функции недоступными извне. Доступ к ним только через строго определенные методы (геттеры и сеттеры). Это помогает контролировать доступ к данным, предотвращая их изменение напрямую.
  ```js
  class Person {
    constructor(name, age) {
      this._name = name; // Инкапсулированные свойства
    }

    // Геттер и сеттер для доступа к закрытому полю
    getName() {
      return this._name;
    }
  
    setAge(name) {
     this._name = name
    }
  }

* ### Наследование
  это механизм, с помощью которого один класс может унаследовать свойства и методы другого класса. Это позволяет создавать новые классы на основе существующих, переиспользуя код.
  ```js
  class Animal {
    constructor(name) {
      this.name = name;
    }

    speak() {
     console.log(`${this.name} makes a noise.`);
    }
  }

  class Dog extends Animal { // Dog наследует Animal
    speak() {
     console.log(`${this.name} name.`);
    }
  }
  
  const dog = new Dog('Bob');
  dog.speak(); // Bob name.

* ### Полиморфизм
  это способность объектов разных классов реагировать на одно и то же действие или метод по-разному. Это достигается через переопределение методов в дочерних классах. Полиморфизм позволяет работать с объектами разных типов одинаково, даже если их поведение различается.

  ```js
  class Animal {
    constructor(name) {
      this.name = name;
    }

    speak() {
      console.log(`${this.name} makes a noise.`);
    }
  }

  class Dog extends Animal {
    speak() {
      console.log(`${this.name} barks.`);
    }
  }

  class Cat extends Animal {
    speak() {
      console.log(`${this.name} meows.`);
    }
  }

  const animals = [new Dog('Buddy'), new Cat('Whiskers')];

  animals.forEach((animal) => {
  animal.speak(); // Buddy barks. Whiskers meows.
  });
  
##  Для восстановления предыдущей версии кода в git после внесения ошибки
 * Если ошибка была внесена в последний коммит, который еще не отправлен на удаленный репозиторий, можно либо исправить коммит, либо откатить его.
   - git commit --amend  исправить коммит
   - git reset --hard HEAD^ откатить изменения
 * Если ошибка отправлена в удаленный репозиторий:
   - git revert <commit_hash> внести изменения и закомитить
 * Также можно использовать Git Rebase:
   - git rebase -i HEAD~3 удалить коммит

## Функцию на JS, которая проверяет, является ли строка палиндромом:
  ```js
    function isPalindrome(str) {

    const cleanedStr = str.toLowerCase().replace(/[^a-z0-9]/g, '');
    return cleanedStr === cleanedStr.split('').reverse().join('');
  }

  console.log(isPalindrome("A man, a plan, a canal: Panama")); //true
  console.log(isPalindrome("Hello")); // false
```
## Мой опыт:
Начал изучать js два года назад, за это время я достиг больших результатов.
Окончил курсы THE ROLLING SCOPES SCHOOL, курс JAVASCRIPT/FRONT-END 2023Q4 2023-2024, ззанял 7 место из более 366 студентов, окончивших курс. 
Далее окончил курс по React и Next js в 2024 заняв 3 место из 389студентов.
Было сделано 2 финальных командных проекта. В обоих проектах был тимлидом, помимо разработки занимался организационными вопросами, а именно: составлением задач для спринтов, распределением задач в команде, организацией процесса разработки и составлением канбан-доски.

Проекты: 

- [Nonograms](https://rolling-scopes-school.github.io/mistert1a-JSFE2023Q4/nonograms/) game: Js
- [Fun chat](https://rolling-scopes-school.github.io/mistert1a-JSFE2023Q4/fun-chat/#) game: Ts
- [Puzzle](https://rolling-scopes-school.github.io/mistert1a-JSFE2023Q4/rss-puzzle/) game: Ts, MVC
- [Async race](https://rolling-scopes-school.github.io/mistert1a-JSFE2023Q4/async-race/) game: Ts
- [Coffe house](https://rolling-scopes-school.github.io/mistert1a-JSFE2023Q4/coffee-house/) Layout: Js
- [Hangman](https://rolling-scopes-school.github.io/mistert1a-JSFE2023Q4/hangman/) game: Js
- [React forms](https://react-task-forms.netlify.app/) app: React, react-hook-form, redux, yup, Ts, jest, vite
- [Planet search](https://next-js-redux-app-cgj1.vercel.app/) app: Next.js, redux, Ts, jest

- [app for Rest and GraphQL requests](https://graphiql-app-kappa.vercel.app/) app: Next.js, Ts, jest, graphql, tailwindcss, next-ui, firebase, react-hook-form, zod, next-ui, next-intl

  Также я сейчас работаю над реализациями нескольких проектов.
