# MyFirstApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.0.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).


## ng-content
Anything between component opening and closing tags (<app></app>) is get lost.
If we want to inject a fragment of html template into child component from parent component, one can use ng-content inside child and specify template in parent with component tags

# VIEW ENCAPSULATION
Angular restricts the css defined with respect to a component to the 
component itself (and not apply it globally - say a css property to p html element)
It does this by assigning a unique add on to css elements which makes each
element of a component unique w.r.t to other element of an another component

## View Child()
In Angular 8+, the @ViewChild() syntax which you'll see in the next lecture needs to be changed slightly:

Instead of:

@ViewChild('serverContentInput') serverContentInput: ElementRef;
use

@ViewChild('serverContentInput', {static: true}) serverContentInput: ElementRef;

## Lifecycle hooks
ngOnChanges: Called after a bound input property changes (e.g. properties decoreated with @Input)

ngOnInit: Executes when the component is initiaised (not rendered in the dom yet ). Object was created basically. Runs After the constructor has been called

ngDoCheck: Runs multiple times for change detection (change in property/template etc.)

ngAfterContentInit: Called after content (ng-content) has been projected into view.

ngAfterContentChecked: Called every time the project content has been checked

ngAfterViewInit: Called after the components view (and child views) has been initiailized

ngAfterViewChecked: Called every time the view (and child views) have been checked

ngOnDestroy: called once the component is about to be destroy