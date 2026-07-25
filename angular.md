Since you have over 10 years of experience, interviewers will usually focus less on basic Angular syntax and more on architecture, performance, RxJS, state management, forms, and debugging.

Here are frequently asked Angular interview questions, grouped by topic.

## 1. Angular Fundamentals

1. What is Angular?
2. What are the main building blocks of Angular?
3. What is a Component?
4. What is a Module?
5. What is a Standalone Component?
6. Difference between Component and Directive.
7. Difference between Directive and Pipe.
8. What is a Service?
9. What is Dependency Injection?
10. What is a Provider?

---

## 2. Lifecycle Hooks

1. Explain all Angular lifecycle hooks.
2. Difference between `ngOnInit()` and constructor.
3. When is `ngOnChanges()` called?
4. Difference between `ngAfterViewInit()` and `ngAfterContentInit()`.
5. What happens during component destruction?
6. When should `ngOnDestroy()` be used?

---

## 3. Data Binding

1. What are the four types of data binding?
2. Difference between interpolation and property binding.
3. Difference between property binding and attribute binding.
4. What is event binding?
5. What is two-way data binding?
6. How does `[(ngModel)]` work internally?

---

## 4. Directives

1. Difference between structural and attribute directives.
2. Explain `*ngIf`.
3. Explain `*ngFor`.
4. Explain `*ngSwitch`.
5. What is `trackBy`?
6. How do you create a custom directive?

---

## 5. Pipes

1. What are pipes?
2. Pure vs Impure pipes.
3. Async pipe.
4. How do you create a custom pipe?
5. Why should impure pipes be avoided?

---

## 6. Routing

1. How routing works.
2. Lazy loading.
3. Route Guards.
4. Types of Route Guards.
5. Resolver.
6. ActivatedRoute vs Router.
7. Route parameters.
8. Query parameters.
9. Child routes.
10. Wildcard routes.

---

## 7. Forms

### Template Driven

* Advantages
* Disadvantages

### Reactive Forms

1. FormGroup
2. FormControl
3. FormArray
4. Validators
5. Custom Validator
6. Async Validator
7. Dynamic Forms
8. PatchValue vs SetValue
9. Reset form
10. Disable controls

---

## 8. Dependency Injection

1. Explain Angular DI.
2. Hierarchical Injector.
3. Root Injector.
4. Component Injector.
5. Constructor Injection.
6. Injection Token.
7. Optional Injection.
8. Multi Provider.
9. useClass
10. useValue
11. useFactory
12. useExisting

---

## 9. RxJS

This is one of the most important interview areas.

1. What is Observable?
2. Promise vs Observable.
3. Subject.
4. BehaviorSubject.
5. ReplaySubject.
6. AsyncSubject.
7. Hot vs Cold Observable.
8. Subscription.
9. Unsubscribe.
10. Memory leaks.

Common operators:

* map
* filter
* tap
* switchMap
* mergeMap
* concatMap
* exhaustMap
* combineLatest
* forkJoin
* zip
* debounceTime
* throttleTime
* distinctUntilChanged
* catchError
* retry
* finalize
* shareReplay

Interview questions:

* Difference between switchMap and mergeMap.
* When to use concatMap.
* Why use exhaustMap in login?
* Explain forkJoin.
* Explain combineLatest.
* Explain shareReplay.

---

## 10. HTTP Client

1. How does HttpClient work?
2. Interceptors.
3. Error Handling.
4. Retry.
5. Global Error Handler.
6. HTTP Headers.
7. HTTP Params.
8. Authentication Token.
9. Refresh Token Flow.
10. File Upload.

---

## 11. Change Detection

Very frequently asked.

1. What is Change Detection?
2. Zone.js.
3. Default Strategy.
4. OnPush Strategy.
5. ChangeDetectorRef.
6. detectChanges().
7. markForCheck().
8. detach().
9. reattach().
10. Performance optimisation.

---

## 12. Component Communication

1. @Input
2. @Output
3. EventEmitter
4. ViewChild
5. ContentChild
6. Template Reference Variable
7. Shared Service
8. RxJS Subject communication

---

## 13. State Management

1. Why NgRx?
2. Redux Principles.
3. Store.
4. Action.
5. Reducer.
6. Selector.
7. Effect.
8. Entity.
9. Signal Store.
10. Component Store.

---

## 14. Angular Signals (Angular 16+)

Very popular now.

1. What are Signals?
2. Writable Signal.
3. Computed Signal.
4. Effect.
5. Signal vs Observable.
6. Signal Input.
7. Signal Output.
8. Signal Forms.
9. Migration from RxJS.
10. Performance benefits.

---

## 15. Performance Optimisation

1. Lazy Loading.
2. Standalone Components.
3. Tree Shaking.
4. TrackBy.
5. Virtual Scrolling.
6. OnPush.
7. Pure Pipes.
8. Async Pipe.
9. Bundle Splitting.
10. Image Optimisation.

---

## 16. Security

1. XSS.
2. CSRF.
3. DomSanitizer.
4. JWT.
5. Route Guards.
6. Content Security Policy.
7. Token Storage.
8. Interceptors.

---

## 17. Angular Architecture

1. Folder structure.
2. Feature modules.
3. Shared module.
4. Core module.
5. Smart vs Dumb components.
6. Reusable Components.
7. Singleton Services.
8. Monorepo.
9. Nx Workspace.

---

## 18. Unit Testing

1. Jasmine.
2. Karma.
3. TestBed.
4. SpyOn.
5. Mock Service.
6. Component Testing.
7. Service Testing.
8. HTTP Testing.
9. Router Testing.

---

## 19. Angular 17/18+ Features

1. Standalone Components.
2. New Control Flow (`@if`, `@for`, `@switch`).
3. Deferrable Views (`@defer`).
4. Signals.
5. Hydration.
6. SSR.
7. Zoneless Angular.
8. Improved Builder.
9. Server Rendering.

---

## 20. Scenario-Based Questions

1. How would you optimise a page with 10,000 records?
2. A component is re-rendering continuously. How would you debug it?
3. How would you share data between unrelated components?
4. How would you implement authentication in Angular?
5. How would you implement role-based access control?
6. How would you cache API responses?
7. How would you cancel previous HTTP requests while typing in a search box?
8. How would you implement infinite scrolling?
9. How would you build dynamic forms from API metadata?
10. How would you prevent duplicate API calls?

---

## 21. Advanced Questions (Lead/Senior Level)

1. Explain Angular's change detection internals.
2. How does Zone.js trigger change detection?
3. Explain the Angular compiler (AOT vs JIT).
4. How does Ivy work?
5. What is tree shaking?
6. How does dependency injection resolution work?
7. Explain hierarchical injectors with examples.
8. How does lazy loading reduce bundle size?
9. How would you structure a large enterprise Angular application?
10. What are common Angular performance bottlenecks and how would you resolve them?

