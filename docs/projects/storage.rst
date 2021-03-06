https://github.com/CenterForOpenScience/osf.io/pull/3855
https://github.com/CenterForOpenScience/osf.io/pull/3847
https://github.com/CenterForOpenScience/osf.io/pull/3712

**Purpose:** The OSF allows users to store, view, and share files. Users can take advantage of the built in OSF Storage or connect to an add-on.

Files can be accessed via the Files Browser available on the :ref:`Project Overview <overview>` or the Files page. A project
or component's files page can be accessed by clicking on "Files" in the grey navigation bar.

OSF Storage is the default file storage tool on the OSF. Users are given 2GB of OSF Storage for free when they create an account.
When a user uploads a file, that uses some of their storage. If a collaborator on a project, however, uploads a file to that project,
it does not affect all contributor's free storage. Files can be up to 128MB.

Files Browser
------------
The Files Browser displays the project tree and, above that, a toolbar with available actions.
The project or component that the user is currently visiting is at the top of the project tree, followed by the files uploaded
to that project/component, then components that are housed within that project/component. The tree continues to extend until
all children have been listed. Every project and component displays its OSF Storage folder
and any contained folders. If any :ref:`add-ons <add-ons>` are connected, they are displayed within the project
or component. To the left of each add-on, project, component, and file is an icon representing the item. Every item in the
tree is labeled with its title. Projects are preceded by a label—"Project:" and components are similarly indicated by a "Component:"
label before their title.

Nested projects, components, add-ons, and files are indented to indicate their hierarchy.
On page load, top level storage add-ons and OSF Storage are expanded, meaning their contents are visible.
Projects and components nested immediately within the top level project/component are expanded as well, as are their storage
add-ons and OSF Storage. Third level components (i.e. children of the currently viewed project/component's children) are not expanded.
Expanded elements are indicated by a minus sign to their left. Collapsed elements are indicated by a plus sign.
Clicking on these symbols expands and collapses the contents. All icons stay the same when their corresponding elements
are open or collapsed. Folders are an exception to this rule: When a folder is expanded, its icon is an open folder.
When a folder is collapsed, its icon is a closed folder.

Double clicking on a project or component returned as a result brings the user to the
corresponding project overview page. Double clicking on a file brings the user to the file's :ref:`details page <files_view>`.
Double clicking on a storage item like an add-on or OSF Storage returns the file tree with the item selected.

There are three columns in the Files Browser: "Name," "Size," and "Downloads." The "Names" column is sortable in alphabetical order. Sorting
by name re-orders files within each project or folder to be in alphabetical or reverse alphabetical order. The "Size" column
lists the file size for each file. The "Downloads" column lists the number of downloads for each file; if there have been no downloads,
the number is O.

By default, the toolbar displays a "Search" button and an information button, indicated by an "i."
Clicking on the information button pulls up a modal that is displayed inside the panel and reads::

    How to Use the Files Browser
    Select Rows: Click on a row (outside the name) to show further actions in the toolbar.
    Select Multiple Files: Use Command or Shift keys to select multiple files.
    Open Files: Click a file name to go to the file.
    Open Files in New Tab: Press Command (or Ctrl in Windows) and click a file name to open it in a new tab.
    Copy Files: Press Option (or Alt in Windows) while dragging a file to a new folder or component.
    [Close]

Searching in the Files Browser
^^^^^^^^^^^^^^^
**Purpose:** The search bar in the Files Browser allows the user to quickly find a file they are seeking.

Clicking the "Search" button opens a text field for the user to enter their query into. The "Search" button disappears when
the text field opens and a cancel button indicated by an 'x' appears to the right. The user can type their query into the text field
and any element in the file tree (projects, components, OSF Storage, add-ons, files) matching the search are displayed in the
Files Browser. Only titles are searched—not file contents. Elements that do not match the query are hidden.
Selecting a result returns the file tree and closes the search field. The selected result is then highlighted within
the file tree.

Uploading to OSF Storage
^^^^^^^^^^^^^^^^^
**Purpose:** Users can upload files to be stored by the OSF.

If the user is a contributor with read+write or admin :ref:`privileges <contributors>`, then selecting an OSF Storage element
adds two additional buttons to the toolbar: "Upload" and "Create Folder."

Clicking the "Upload" button will open a file selector that allows the user to search their
computer to select files for upload. Any file type can be uploaded. Folders cannot be uploaded. While a file is uploading,
the title is displayed in the storage folder it is being uploaded to. A progress bar indicates the file's upload progress.
An 'x' button to the right of the upload bar allows the user to cancel the upload.

Users can also drag and drop a file to be uploaded into any storage add-on or OSF Storage folder that they have read+write or
admin privileges on.

.. _folders:

Folders
^^^^^^^^^
**Purpose:** Folders allow users to organize items within a project or component's OSF Storage.

Clicking the "Create Folder" opens a text field and two buttons that replace the existing buttons in the toolbar: a "Create" and a
cancel button labeled with an 'x.'  The user can type a folder name into the text field and press the return key or click "Create"
to save the change. Folder titles can be any length; if they are too long to fit in the panel, an ellipsis cuts of the excluded content.
The folder appears, collapsed, within the OSF Storage folder selected. Any number of folders can be created. Folders can be nested
within one another.

Clicking on a folder shows the "Upload," "Create Folder," "Search," and "i" buttons in the toolbar as well as two additional options:
"Delete Folder" and "Rename."

Clicking "Rename" opens a text field with the current folder title editable within it. A "Rename" button
allows the user to confirm the changes and an 'x' button cancels the changes. If the user attempts to rename the folder but leaves
the text field empty, no changes are saved. After renaming a folder, before showing the newly renamed folder, the folder's row in the table reads::

    Successfully renamed.

Clicking the "Delete Folder" option opens a modal within the Files Browser::

    Delete "[folder name]"?
    This folder and ALL its contents will be deleted. This action is irreversible.
    [Cancel][Delete]

Confirming the deletion removes the folder and all contained files from the Files Browser.

Clicking on an expanded folder or OSF Storage folder that has files contained within it adds one additional button to the toolbar—"Download as zip."
Clicking this button immediately issues the download of a zip file containing all files and folders that were housed within the selected
element. On refresh, the download count for each file in the folder is incremented by one.

Single File Actions
^^^^^^^^^^^^^
Selecting a single file from any add-on or folder adds four additional buttons to the toolbar, beyond the default "Search" and "i:"
"Download," "View," "Delete," and "Rename."

Clicking the "Rename" button when a file is selected opens a text field with the current folder title editable within it. A "Rename" button
allows the user to confirm the changes and an 'x' button cancels the changes. If the user attempts to rename the file but leaves
the text field empty, no changes are saved. After renaming a file, before showing the newly renamed file, the file's row in the table reads::

    Successfully renamed.

.. todo:: you can change file types by renaming the file but it corrupts them

Clicking the "Delete" button when a file is selected opens a modal within the Files Browser::

    Delete "[file name]"?
    This action is irreversible.
    [Cancel][Delete]

Confirming the deletion removes the file from the Files Browser.

Clicking the "View" button brings the user to the file's :ref:`Details page <details>`.

Clicking the "Download" button downloads the file. On refresh, the download count for the file increments by one.

Multiselection of items
^^^^^^^^^^^^^^^
**Purpose:** Selecting multiple items at once allows users to perform batch actions.

Users can select multiple items by holding down the Command or Shift keys.

When multiple items are selected, a "Delete Multiple" button shows in the toolbar. Clicking this button opens a modal
within the Files Browser that reads::

    Delete multiple files?
    This action is irreversible.
    [list of items being deleted]

    [Cancel][Delete All]

If one of the selected items is a folder, the modal contains an extra warning::

    Some of the selected items are folders. This will delete the folder(s) and ALL of their content.

Only files and folders from within the same project or component can be multi-selected.

Multiple files cannot be downloaded at once unless they are in a :ref:`folder <folders>`.


Storage Add-Ons
----------
**Purpose:** Storage add-ons can be used to connect a user's OSF account to another file storage system, increasing their
capacity to share files via the OSF and bringing more functionality to their projects.

Information on connecting add-ons to user accounts :ref:`can be found here. <user-addon>` Information on individual add-on's
behavior :ref:`can be found here. <add-ons>`