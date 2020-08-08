## Scripting

Occasionally, you want to create additional gameplay (especially when creating a story campaign). This section highlights additional functions you can call from blueprints, as well as events you may handle.

Feel free to explore the plugin yourself by looking at what other functions and events each component provides, and open an issue if you're missing something.

Also note that much gameplay of the plugin relies on [Gameplay Tags](https://docs.unrealengine.com/en-US/Gameplay/Tags/index.html) as defined by `Content\Data\DT_RTSGameplayTags.uasset`. This enables you to create unique gameplay and abilities by applying/removing these tags to/from the `URTSGameplayTagsComponent` of your actors. Initially, many of the plugin components apply matching gameplay tags (e.g. `Status.Permanent.CanAttack` from `RTSAttackComponent`). When creating your own actor components, you can derive from `RTSActorComponent` to provide your own _Initial Gameplay Tags_ as well. The plugin also provides an own [Gameplay Debugger](https://docs.unrealengine.com/en-US/Gameplay/Tools/GameplayDebugger/index.html) category for checking the gameplay tags of selected actors.


### RTSBountyComponent
#### Events

| Event | Description |
| --- | --- |
| ![On Bounty Collected](Images/OnBountyCollected.png) | Event when the bounty was collected. |


### RTSContainerComponent
#### Functions

| Node | Description |
| --- | --- |
| ![Load Actor](Images/LoadActor.png) | Adds the specified actor to this container. |
| ![Unload Actor](Images/UnloadActor.png) | Removes the specified actor from this container. |


### RTSConstructionSiteComponent
#### Events

| Event | Description |
| --- | --- |
| ![On Construction Finished](Images/OnConstructionFinished.png) | Event when the construction timer has expired. |


### RTSGameMode
#### Functions

| Node | Description |
| --- | --- |
| ![Transfer Ownership](Images/TransferOwnership.png) | Sets the specified player as the owner of the passed actor. |


### RTSGameplayLibrary
#### Functions

| Node | Description |
| --- | --- |
| ![Is Visible For Actor](Images/IsVisibleForActor.png) | Checks whether Other is visible for Actor. |


### RTSGameplayTagLibrary
#### Functions

| Node | Description |
| --- | --- |
| ![Add Gameplay Tag](Images/AddGameplayTag.png) | Applies the passed gameplay tag to the specified actor. |
| ![Get Gameplay Tags](Images/GetGameplayTags.png) | Gets the current set of gameplay tags of the specified actor. |
| ![Has Gameplay Tag](Images/HasGameplayTag.png) | Checks whether the specified actor currently has the passed gameplay tag applied. |
| ![Remove Gameplay Tag](Images/RemoveGameplayTag.png) | Removes the passed gameplay tag from the specified actor. |


### RTSHealthComponent
#### Events

| Event | Description |
| --- | --- |
| ![On Health Changed](Images/OnHealthChanged.png) | Event when the current health of the actor has changed. |
| ![On Killed](Images/OnKilled.png) | Event when the actor has been killed. |


### RTSPawnAIController
#### Functions

| Node | Description |
| --- | --- |
| ![Issue Order](Images/IssueOrder.png) | Makes the pawn carry out the specified order. |
| ![Issue Attack Order](Images/IssueAttackOrder.png) | Makes the pawn attack the specified target. |
| ![Issue Begin Construction Order](Images/IssueBeginConstructionOrder.png) |  Makes the pawn construct the specified building at the passed location. |
| ![Issue Gather Order](Images/IssueGatherOrder.png) | Makes the pawn gather resources from the specified source. |
| ![Issue Move Order](Images/IssueMoveOrder.png) | Makes the pawn move towards the specified location. |
| ![Issue Stop Order](Images/IssueStopOrder.png) | Makes the pawn stop all actions immediately. |

#### Events

| Event | Description |
| --- | --- |
| ![On Order Changed](Images/OnOrderChanged.png) | Event when the pawn has received a new order. |


### RTSPlayerController
#### Events

| Event | Description |
| --- | --- |
| ![On Player State Available](Images/OnPlayerStateAvailable.png) | Event when the player state has been set up or replicated for this player. |


### RTSPlayerResourcesComponent
#### Functions

| Node | Description |
| --- | --- |
| ![Add Resources](Images/AddResources.png) | Adds the specified resources to the stock of this player. |

#### Events

| Event | Description |
| --- | --- |
| ![On Resources Changed](Images/OnResourcesChanged.png) | Event when the current resource stock amount for the player has changed. |


### RTSPlayerController
#### Functions

| Node | Description |
| --- | --- |
| ![Get Own Actors](Images/GetOwnActors.png) | Gets the list of actors currently owned by this player. |


### RTSProductionComponent
#### Events

| Event | Description |
| --- | --- |
| ![On Production Finished](Images/OnProductionFinished.png) | Event when the production timer has expired. |
