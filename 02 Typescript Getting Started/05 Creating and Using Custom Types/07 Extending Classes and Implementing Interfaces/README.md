# 07 Creating and Using Custom Types - Extending Classes and Implementing Interfaces

- Use keyword **extends** for extend the class

```javascript

class WebDeveloper extends Developer {
    favoriteEditor: string;
    writeTypeScript(): void {
        // write awesome code
    }
}
let webdev: WebDeveloper = new WebDeveloper();
webdev.department = 'Software Engineering';
webdev.favoriteEditor = 'Visual Studio Code';

```
### Implementing an Interface

```javascript
class WebDeveloper extends Developer {
    favoriteEditor: string;
    writeTypeScript(): void {
        // write awesome code
    }
}
let webdev: WebDeveloper = new WebDeveloper();
webdev.department = 'Software Engineering';
webdev.favoriteEditor = 'Visual Studio Code';


interface Employee {
    name: string;
    title: string;
    logID: () => string;
}

class Engineer implements Employee {
    name: string;
    title: string;
    logID() {
        return `${this.name}_${this.title}`;
    }
}
```