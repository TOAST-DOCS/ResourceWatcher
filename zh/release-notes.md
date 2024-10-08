## Governance & Audit > Resource Watcher > Release Notes

### July 23, 2024

#### Feature Updates

- [Console] Improved the feature to view deleted resources on the Resource page
- [Console] Changed the format of resource tags to {key:value}.
  - Changed the settings screen (modal window) for creating and modifying resource tags to create and modify tags of the form {key:value}.
  - Changed the settings screen (modal window) for setting resource tags to create and modify tags of the form {key:value}.
  - Changed the area for selecting resource tags on the settings screen (modal window) for creating and modifying resource groups.
  - Changed the area for selecting resource tags on the settings screen (modal window) for creating and modifying notifications.

#### Added Features

- [Console] Added the feature to view the change history of resource groups and resource tags assigned to a resource.
- [Console] Added the feature to view the change history of resource tags.

### June 11, 2024

#### Feature Updates

- Applied roles and permissions.
- Added the information on permissions required for API calls.

### April 23, 2024

#### Feature Updates

- Changed the NCRN format to enhance security.
  - Removed the appKey information.
- Removed the constraint that the service is not available in the IAM Cloud Console.


### February 27, 2024

#### Feature Updates

- Improved to view the detailed history of an notification when navigating to the console from the notification history screen.
- Modified the defaults of calendar search filters in each list according to the purposes.
  - Modified to view the period from organization creation date to view date when viewing the entire period.
  - Fixed the event lookup period for resources to only be selectable up to the last 3 months.
    - Fixed the event lookup period so that you can only select the last 3 months. If you selected a time period longer than 3 months, you could only see the last 3 months.
- Improved to add recipients, events, and resources when creating notifications.
  - Select only the receive method to add the items. Previously, you needed to take two steps, selecting the receive method and clicking the add button.

### November 14, 2023.

#### Feature Updates

- Improved the ability to select multiple events when setting up notifications.
  - Notification rules are no longer selectable.
- Improved to allow you to select `All Resources` and `All Events` when setting up notifications.

### December 13, 2022

#### Added Features

- Resource Watcher service released
