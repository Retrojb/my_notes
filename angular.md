# Architecture
#Angular #architecture
#observables an array of data streamed over time, you subscribe to loop thru the data 
#ContainerComponent HOW TO #RETRIEVEDATA AND #ROUTE
 vs #presentationalComponent #INPUTDATA #DISPLAYDATA #EVENTS

#ContainerComponent: These components know HOW TO #RETRIEVEDATA from the service layer. Note that the top-level COMPONENT OF A #ROUTE is usually a Container Component, and that is why this type of components where originally named like that.

#presentationalComponent these components simply take DATA AS INPUT and know HOW TO DISPLAY it on the screen. They also can EMIT CUSTOM #EVENTS

#ContainerComponent
#### Top Level Container Component
	1. component declares a few #observables on ngOnInit, that are derived from other observables obtained from the service layer
	2. component will be displayed without any data initially, and it will do one or more calls to the service layer to fetch the data.
##### Top level template contianer 
#HTML #Angular 
``
<course-detail-header [course]="course$ | async" [lessons]="lessons$ | async"
[firstName]=“(user$  | async).firstName" (subscribe)="onSubscribe($event)">
</course-detail-header>
``
#observables are being subscribed to through the async #AngularPipes data is based to the `course-detail-header` they are in charge od retrieving the data for the top level


Global #errorHelpers with Uncaught Reference global is not defined on packages: #Angular #AngularError
add this to the `polyfill.ts` file
`(window as any)['global'] = window;`
rebuild