# Nansen.AdminTools.ContentUsage 
#### v1.1.0

## Find Content Usages Manual
--------------------------
This document provides basic instructions for using the Find Content Usages tool versions 1.0.0 through 1.0.1.

## Location
-----------------
The tool is available to WebAdmins through the CMS Admin panel. It can be found on the "Admin" tab under "Tools".

## Search Parameters
-----------------
The first two fields are required for search. The search button is disabled until they are provided.

* *Base Type Selection* - (Required Field) The first dropdown you are presented with is the base content type selector. It will be defaulted to "Select Content Type". You will be required to select from the available types, which are Pages, Blocks, and Media. Once selected, a secondary dropdown will appear with content types that are descendents of the selected type.

* *Content Type Select* - (Required Field) This field will be populated with content types based on the previously selected field. 
						It will contain descendents of either Page, Block, or Media base types. This selected content 
						type is what will be populated in the final usage results.

* *Language Select* - (Optional) This field will be populated with the available languages on the site. This field is optional, and is a way for you to further narrow down your results.

* *Excluding* - (Optional) A collection of checkboxes that allow you to exclude certain pages based specific statuses. You can exclude pages based on deleted pages, expired pages, pages that fetch data, and pages that are shortcuts.

* *Property Filtering* - (Optional) The "+ Add property filter" link will dynamically add dropdowns based on the available properties for the previously selected content type. Based on the type of property, you will be provided with different options for creating conditionals based on the property values. 

## Results
-----------------
Results will be provided in a table format with the following columns:

### Id
This is the content Id of the provided result

### Status
This is the status of the content result. 
* *NotCreated* - The item or language has not been created,
* *Rejected* - The version was rejected rather than published, and returned to the writer.
* *CheckedOut* - The version is currently in progress.
* *CheckedIn* - A writer has checked in the version and waits for the version to be approved
* *Published* - The currently published version.
* *PreviouslyPublished* - This version has been published previously but is now replaced by a more recent
* *DelayedPublish* - This version will be automatically published when the current time has passed the Start Publish date.
* *AwaitingApproval* - The version is awaiting approval
* *Trash* - The item has been moved to Trash.
* *Expired* - The item's StopPublish value is in the past. 

### Name
The Content Name property. This serves as a link to the provided edit content page in the CMS.

### Implemented in Languages
The languages that the content was implemented in. These serve as links to the provided edit page
							in the CMS for those content items.

### Languages with Matching Property
Based on the property filtering, this will list any languages that the content exists in that
									 pass the specified conditions.

### Referenced on
Provides a list of content items that reference this piece of content. Each result serves as a link to the 
					edit page of the content that references this result.
