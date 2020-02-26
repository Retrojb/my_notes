
# Angular architecture


### Observables:
   * an array of data, streamed over time. you subscribe to loop thru the data 
   * observables are subscribed to through the async **AngularPipes** 
   
### Container / Feature Components:

Laymans terms: **RETRIEVE DATA** from the service layer and handle **ROUTES**
   * Note that the top-level COMPONENT OF A #ROUTE is usually a Container Component, and that is why this type of components where originally named like that.

#### Top Level Container Component
	* component can declare several observables on `ngOnInit()`, they're derived from observables obtained from the service layer
	* component will be displayed without any data initially, and it will do one or more calls to the service layer to fetch the data.
	
 **Top level template contianer**
 
``
<course-detail-header [course]="course$ | async" [lessons]="lessons$ | async"
[firstName]=“(user$  | async).firstName" (subscribe)="onSubscribe($event)">
</course-detail-header>
``

# ContainerComponent

#### Presentational Components
Laymans terms: these components simply take DATA AS INPUT and know HOW TO DISPLAY it on the screen. They also can EMIT CUSTOM EVENTS



Global #errorHelpers with Uncaught Reference global is not defined on packages: #Angular #AngularError
add this to the `polyfill.ts` file
`(window as any)['global'] = window;`
rebuild


event emitter is a wrapper for the RxJS `Subject` class

EventEmitter<T> extends Subject<T> { ... }

RxJS Subject class => subject is an observable.
subjects are subscribed to you have to provide an observable (recieves values normally)
the subscribe doesn't invoke a new execution, just registers the observable.


subscribtion is an obj, that represents a disposable resource (the observable execution).
unSubscribe() no arguements required => releases resources / cancels the executed observable
    take(n): emits N values before stopping the observable.
    takeWhile(predicate): tests the emitted values against a predicate, if it returns `false`, it will complete.
    first(): emits the first value and completes.
    first(predicate): checks each value against a predicate function, if it returns `true`, the emits that value and completes.
        * RxJS should use teakUntil(n) or takeWhile( if (condition > n) {x => x.unSubscribe()})
