# angular-myfirstcomponent

Component contains template, class and metadata.
Component must be declared in module. In our example 'MyFirstComponentComponent' is added under declarations in app.module.ts. In order to add in module we need to import from it's physical location.
Class is decorated with @Component decorator. Decorator is function that adds metadata to a class, its members or its method arguments. Decorator is prefixed with @.
Value of selector is a directive name used in html. In our example 'app-my-first-component' is a directive name used in app.component.html

Command to create component : ng g c my-first-component

my-first-component.component.ts

```js
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-my-first-component',
  templateUrl: './my-first-component.component.html',
  styleUrls: ['./my-first-component.component.css']
})
export class MyFirstComponentComponent implements OnInit {

  constructor() { }

  ngOnInit() {
  }

}
```

my-first-component.component.html

```html
<div>
  my-first-component works!
</div>
```

app.module.ts

```js
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { FormsModule } from '@angular/forms';

import { AppComponent } from './app.component';
import { MyFirstComponentComponent } from './my-first-component/my-first-component.component';

@NgModule({
  imports: [BrowserModule, FormsModule],
  declarations: [AppComponent, MyFirstComponentComponent],
  bootstrap: [AppComponent]
})
export class AppModule {}
```

app.component.html

```html
<app-my-first-component></app-my-first-component>
```
