# How to use

Add a link tag with [flag-icon-css](https://cdnjs.com/libraries/flag-icon-css) library to your index.html file.

Add **NgxSelectFlagsModule** to your module in the import section.

After:

```
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  template: `
    <ngx-select-flags
      [selectedCountryCode]="selectedCountryCode"
      [countryCodes]="countryCodes"
      (changedCountryCode)="changeSelectedCountryCode($event)">
    </ngx-select-flags>
    <h1>{{ selectedCountryCode }}</h1>
  `
})
export class AppComponent {
  selectedCountryCode = 'us';
  countryCodes = ['us', 'lu', 'de', 'bs', 'br', 'pt'];

  changeSelectedCountryCode(value: string): void {
    this.selectedCountryCode = value;
  }
}
```

## [Demo](https://artyomgr.github.io/ngx-select-flags/)