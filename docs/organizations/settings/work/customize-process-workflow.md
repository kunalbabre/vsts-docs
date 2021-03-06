---
title: Customize the workflow of an inherited process
titleSuffix: Azure DevOps Services
description: Add workflow states to a work item type for an inherited process for a project
ms.technology: devops-agile
ms.prod: devops
ms.assetid: 35971F8F-26EF-4C99-9825-4AC072A6EBE4  
ms.manager: douge
ms.author: kaelliauthor: KathrynEE
monikerRange: 'vsts'
ms.topic: conceptual
ms.date: 05/31/2018
---

# Customize the workflow 

[!INCLUDE [temp](../../../_shared/version-vsts-only.md)]


Each work item type is associated with a workflow that supports tracking the status of work as it moves from creation to completion. To support your business and team processes, you can add custom states to most work item types (WITs). For example, you may want to insert a Triaged state for bugs, or a Design state for features or user stories. 

Here, the Bug WIT has been customized to support a Triaged state. The state and reason fields appear on the work item form in the header area.

<img src="_img/process/cust-workflow-form-triage-header.png" alt="Bug work item form, header area" style="border: 1px solid #C3C3C3;" /> 

> [!NOTE]    
> Before adding a workflow state, review [Workflow states and state categories](../../../boards/work-items/workflow-and-state-categories.md) to learn how workflow states map to state categories. 

[!INCLUDE [temp](../_shared/process-prerequisites.md)] 

[!INCLUDE [temp](../_shared/open-process-admin-context-ts.md)]

[!INCLUDE [temp](../_shared/automatic-update-project.md)] 

<a id="states">  </a>
<a id="add-states"></a>
## Add a workflow state   

States you add will appear in the picklist for the States field shown in work item forms and the query editor. A transition to and from the State you add is created to every other State, except not to a Removed state. Also, default reasons are defined, such as Moved to state Triaged, Moved out of state Triaged.

> [!NOTE]    
> States that you add to the task WIT will add columns to the task board. If you [track bugs along with tasks](../show-bugs-on-backlog.md), then states you add to the bug WIT will also add columns to the task board. You don't have to add the same states to each of these WITs, however, you may want to do so in order to  update the status in the same way and to minimize the number of columns that get added.  
>
> If you add a state to a WIT which you is associated with a backlog level, each team will need to update their [Kanban board columm settings](../../../boards/boards/add-columns.md) in order to view and use the affected Kanban board.  

0. From the **Work Item Types** page, choose the work item type you want to modify, choose **States**, and then choose **New State**.    

	> [!div class="mx-imgBorder"]  
	> ![Process page, Bug WIT, States tab, Add state](_img/process/cpworkflow-add-state.png) 

0. Enter the name of the State, choose its category and color, and then click **Save**. The color you specify will appear throughout the product including on the work item form and when the State field appears on a backlog, boards, query results, and more.  

	<img src="_img/process/cpw-new-state-triaged.png" alt="State dialog box" style="border: 1px solid #C3C3C3;" />  

	> [!NOTE]   
	> You can't change the order of states. States are listed in the order you add them within the **States** page, and they're listed alphabetically within the drop down list of a work item form).  
	
0. When you've finished adding states for the WIT, verify your changes by refreshing your browser and open a work item of the type you just customized. 

	Here we show the state drop down field with Triaged selected. 

	> [!div class="mx-imgBorder"]  
	> ![Bug form, Triaged state added](_img/process/cpw-added-triage-state-in-form.png) 

0. Remember, when you add a state to a WIT which is associated with a backlog level, each team that uses the Kanban board will need to [update their column settings](../../../boards/boards/add-columns.md).

<a id="edit-state"></a>
## Edit a state

You can edit the category or the color of a custom state. However, you can't change the name of the custom state. 

0. Choose **Edit** from the &hellip; context menu for the state you want to modify.  
  
	<img src="_img/process/cpworkflow-edit-state.png" alt="Bug WIT, Edit custom state" style="border: 1px solid #C3C3C3;" /> 

0. Modify the category or color, and then click Save. 

0. If you change the category, teams that use the Kanban board to update their status will need to update their [column settings](../../../boards/boards/add-columns.md).    
 
<a id="remove-state"></a>
## Hide or remove a state

When you hide or remove a state:  
- The state no longer appears in the State picklist for the WIT
- No changes occur to the work item history     
- Existing work items maintain their state value, but are in an invalid state. If you want to make a change to the work item, you must first update the state values. You may want to create a query and do a bulk update to move the affected work items into a valid state. If you add the state back to the work item type, the work items revert to a valid state.  
 

<a id="hide-state"></a>
## Hide or unhide an inherited state 

You can hide an inherited state that your team doesn't use in its workflow process. However, you must have at least one state defined for each category. 

0. Open the &hellip; context menu for the state you want to hide and choose the **Hide** option. 

	Here we hide the Resolved state for the Bug WIT. 

	<img src="_img/process/cpworkflow-hide-state.png" alt="Hide an inherited state" style="border: 1px solid #C3C3C3;" /> 

	> [!NOTE]    
	>If you hide the state of a WIT tracked on a Kanban board, each team  that uses the Kanban board will need to [update their column settings](../../../boards/boards/add-columns.md).

0. To unhide, open the &hellip; context menu and choose the **Unhide** option.  
 

<a id="remove-state"></a>
## Remove a custom state 
0. Open the &hellip; context menu for the state you want to remove, and choose **Remove**. You can only remove a custom state.     

0. From the Remove State dialog, click **Remove**.   

	<img src="_img/process/workflow-remove-state-warning.png" alt="Remove state warning dialog box" style="border: 1px solid #C3C3C3;" />  

0.  If teams use the Kanban board to update their status, each team will need to update their [column settings](../../../boards/boards/add-columns.md).    
 

## Related articles   

- [Add or modify a work item type](customize-process-wit.md)
- [Add and manage fields](customize-process-field.md)  
- [Customize a form](customize-process-form.md)
- [Customize a project using an inherited process](customize-process.md) 
- [Add or edit Kanban columns](../../../boards/boards/add-columns.md)  
- [Query by workflow or Kanban board changes](../../../boards/queries/query-by-workflow-changes.md)    











