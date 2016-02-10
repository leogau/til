# Create Observable From CodeMirror Event

CodeMirror has it's own event system where events are registered like

```js
editor.on('change', callback)
```

To use make this an observable

```js
import {Observable} from 'rxjs/Observable'
import 'rxjs/add/observable/fromEvent'
import 'rxjs/add/operator/throttleTime'

//as you were doing
let editor = CodeMirror.fromTextArea(this.field.nativeElement);

//wrap into an Observable
let changes = Observable.fromEvent(editor, 'changes');

//throttle and pipe into event emitter (16ms is roughly 60fps)
changes.throttleTime(16).subscribe(modelChanges);
```

[Source](https://github.com/angular/angular/issues/6103#issuecomment-167025061)
