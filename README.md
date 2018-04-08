# AndroidFeatureChecklist
A checklist to help breakdown feature/screen work into workable tasks in an MVP architecture

* Model
  * Is this data static or dynamic?
  * If the data isn’t hardcoded into the app, it’s dynamic.
  * Who owns the data?
  * What does it look like?
  * When will it be available?
  * Do we have QA/mock data available?
  * Do we need to generate mock data ourselves?
  * Are any fields optional or nullable?
  * Should default values be used in empty/null cases? What are the defaults?
  * Will any localization be needed?
  * Does any data come from the user?
  * Do we need to do any validation?
  * How long is the data valid for?
  * Is there refresh logic?
  * Is there paging logic?
* View
  * Entrance/Exit transitions
    * How to we enter this screen?
    * What does it look like?
    * Is there anything on the previous screen that matches this screen that we can use for a shared element transition?
  * What does the layout look like for the following basic UI/Data states?
    * Empty
    * Failure
    * Stale
    * Loading
    * Partially loaded
    * Fully loaded
    * Are there additional states?
  * Can anything scroll?
  * Can anything be clicked?	
  * Does anything shrink/grow/change position?
* Presenter
  * Lifecycle
    * What happens on backgrounding/foregrounding the app?
    * What happens when the app is killed on this screen?
    * What data/state information should be persisted between pause/resume, stop/restart?	
  * What happens onClicks?
    * What action should be taken (network/ui)?
  * What animation should be used to show instant/asynchronous actions?
  * What outside dependencies can influence the state of this screen?
    * Settings/Preferences
    * Network connectivity
    * External configuration files
    * Localization
* Service layer/Interactor
  * What type of endpoint is this? REST/GraphQl/Protocall Buffers/websocket
  * How is the request formatted?
  * How is the response formatted?
  * Is this a single request/response or a stream of responses?
  * What sort of data transformations need to be done to map the response data to the required 
  * Are any special libraries required to access this endpoint?
  * Is authorization required, if so how is it obtained?


