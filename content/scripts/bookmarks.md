---
title: "Bookmarks"
date: 2023-08-16T15:28:03+01:00
---

---
{{< center alt="text"  src="/under.gif">}}

{{< space >}}

<!--


{{< centered-big-title size="30px" color="#5C5CFF" title="Bookmarks Manager Script" align="center" >}}

{{< centered-big-title size="25px" color="#5C5CFF" title="Introduction" align="left" >}}

The Bookmarks Manager script is a powerful tool designed to help you efficiently organize and manage your bookmarks, links, texts, and PDFs. Whether you're a researcher, developer, or avid internet user, this script enhances your digital organization and productivity by providing a streamlined way to save, categorize, and access important information.

{{< centered-big-title size="25px" color="#5C5CFF" title="What the Script Does" align="left" >}}

The Bookmarks Manager script offers a range of features to simplify your bookmarking and management tasks:

- **Bookmarking:** Easily add links, texts, and PDFs to your bookmarks collection for quick retrieval.
- **Categorization:** Group your bookmarks into categories such as links, texts, and PDFs, ensuring seamless organization.
- **Deletion:** Remove unwanted bookmarks effortlessly, keeping your collection clutter-free.
- **Clipboard Integration:** Capture clipboard contents and instantly convert them into bookmarks.
- **Dynamic Interaction:** Utilize dynamic menus powered by `dmenu` for intuitive interaction.

{{< centered-big-title size="25px" color="#5C5CFF" title="How to Use the Script" align="left" >}}

To seamlessly manage your bookmarks, integrate the Bookmarks Manager script into your workflow using various methods:

- **WM Keybind Integration:** Add the script to your window manager's configuration file to execute it with a keybind. For example, if you're using `dwm`, you can include the following:

  {{< stylish-code >}}
  static const char *bookmarks_cmd[] = { "st", "-e", "sh", "-c", "bookmark.sh", NULL };
  ...
  { MODKEY, XK_b, spawn, {.v = bookmarks_cmd } },
  {{< /stylish-code >}}

  This associates the `MODKEY` and `b` keys to launch the script.

- **Dynamic Menu Integration:** Use a dynamic menu tool like `dmenu` to quickly access the script's features. Launch the script in a terminal by running:

  {{< stylish-code >}}
  bookmark.sh
  {{< /stylish-code >}}

  This will display a dynamic menu where you can choose options.

- **Creating the Bookmarking File:**

  The script relies on a `bookmarking.txt` file to manage your bookmarks. The file should follow this format:

  {{< stylish-code >}}
  Name of Bookmark|https://www.example.com
  Another Bookmark|This is a text bookmark.
  PDF Bookmark|/path/to/your/file.pdf
  {{< /stylish-code >}}

  - For links: Use the name of the bookmark followed by a vertical bar (`|`) and the link.
  - For text: Use the name followed by a vertical bar and the text content.
  - For PDFs: Use the name followed by a vertical bar and the file path.

- **Adding Bookmarks:**

  1. Launch the script using your chosen method.
  2. Select "Add Clipboard" to add clipboard contents as bookmarks.
  3. Provide a distinctive name for the bookmark.
  4. Depending on the content, the script will categorize links, texts, and PDFs.

  Example for adding a link bookmark:

{{< stylish-code >}}
Example Link|https://www.example.com
{{< /stylish-code >}}

  Example for adding a text bookmark:

  {{< stylish-code >}}
  Important Note|Remember to complete the report by Friday.
  {{< /stylish-code >}}

  Example for adding a PDF bookmark:

{{< stylish-code >}}
My PDF|/path/to/your/file.pdf
{{< /stylish-code >}}

- **Deleting Bookmarks:**

  1. Run the script as directed earlier.
  2. Choose "Delete Bookmark" from the menu.
  3. Select the bookmark you want to remove.

- **Clipboard Integration:**

  The script can add the current clipboard contents as bookmarks when you select "Add Clipboard."

Remember to adapt these examples to match your preferred window manager and personal workflow.


{{< centered-big-title size="25px" color="#5C5CFF" title="Documentation" align="left" >}}

For a more detailed understanding of using and customizing the script, refer to this explanatory [PDF 
guide](/path/to/your/bookmarks_manager_guide.pdf) for a deeper exploration of its capabilities.

{{< centered-big-title size="25px" color="#5C5CFF" title="Notes" align="left" >}}

- Ensure you have `dmenu` and `xclip` installed for seamless functionality.
- Feel free to modify the script to align with your workflow and preferences.


visit the [GitHub repository](https://github.com/yourusername/bookmarks-manager) of the script.

---
-->
