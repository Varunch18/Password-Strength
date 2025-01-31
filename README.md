# Password Strength Meter For angular 6

To display the strength of the password with a visual feedback.

[Password Strength Meter](https://www.npmjs.com/package/angular-password-strength-meter) use [zxcvbn](https://github.com/dropbox/zxcvbn) to estimate the strength of the password and also provide a visual feedback with suggestions and warning messages.

This lib was developed based on the following [tutorial](https://scotch.io/tutorials/password-strength-meter-in-angularjs).

How then is password strength measured? `Dropbox developed an algorithm for a realistic password strength estimator inspired by password crackers. This algorithm is packaged in a Javascript library called zxcvbn. In addition, the package contains a dictionary of commonly used English words, names and passwords.`

# Demo

[See Demo Here](https://antoantonyk.github.io/password-strength-meter/)

```html
  <password-strength-meter [password]="password"></password-strength-meter>
```

## Get Started

**Step 1:** Since this lib was depending upon the [zxcvbn](https://github.com/dropbox/zxcvbn) lib, install it first

```sh
npm install zxcvbn@4.4.2 --save
```

**Step 2:** Install password-strength-meter

```sh
npm install angular-password-strength-meter --save
```

**Step 3:** Import Password Strength Meter Module into your app module

```ts
....
import { PasswordStrengthMeterModule } from 'angular-password-strength-meter';

....

@NgModule({
    ...
    imports: [
        ....
        PasswordStrengthMeterModule
    ],
    ....
})
export class AppModule { }
```

**Step 4:** use the password-strength-meter component in your app.component.ts

```ts
  <password-strength-meter [password]="password"></password-strength-meter>
```

## API

| option            |   bind   |   type   |                          default                           | description                                                                                                             |
| :---------------- | :------: | :------: | :--------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------- |
| password          | Input()  |  string  |                             -                              | password to calculate its strength                                                                                      |
| minPasswordLength | Input()  |  number  |                             8                              | min length of password to calculate the strength                                                                        |
| enableFeedback    | Input()  | boolean  |                           false                            | to show/hide the suggestions and warning messages                                                                       |
| colors            | Input()  | string[] | ['darkred', 'orangered', 'orange', 'yellowgreen', 'green'] | to overide the meter colors, password strength range is 0 - 4, for strength 0 equals first color in the array and so on |
| strengthChange    | Output() |  number  |                             -                              | emits the strength of the provided password in number -> range 0 - 4                                                    |
"# Password-Strength" 
"# Password-Strength" 
