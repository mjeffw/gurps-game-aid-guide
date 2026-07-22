Foundry supports PDF files as Journal Entry pages.

## Import a PDF File

This is a GM only function.

### 1. Create a Journal Entry

To import a PDF into Foundry, click the **Journal** button in the right-hand toolbar:
![Pasted image 20260720124658.png](../images/Pasted%20image%2020260720124658.png)

In the Journals sidebar, click on **Create Item** (or select an existing Journal Entry).
![Pasted image 20260720125007.png](../images/Pasted%20image%2020260720125007.png)

Enter a name for the Journal Entry.
![Pasted image 20260720125147.png](../images/Pasted%20image%2020260720125147.png)

A common suggestion is to collect all of your PDFs into a single Journal Entry, and to give that  Journal Entry a name like "PDFs".

![Pasted image 20260720125315.png](../images/Pasted%20image%2020260720125315.png)

## 2. Add a Page

In the Journal Entry page, click the **Add Page** button.

![Pasted image 20260720125420.png](../images/Pasted%20image%2020260720125420.png)

Give the Journal Page a name (typically the name of the PDF) and set the Type to **PDF**.

![Pasted image 20260720125554.png](../images/Pasted%20image%2020260720125554.png)
In the Journal Page editor, set the **PDF Source** to the filesystem path to the PDF file. This path is relative to your Foundry data directory, and (for security reasons) you cannot choose a file outside of that at all. But read on ...

Click on the File icon in the PDF Source entry to get a Document Browser. You can either select a PDF file from here, or you can upload one.

### Uploading a PDF

By default you will get a Document Browser like this:
![Pasted image 20260720130525.png](../images/Pasted%20image%2020260720130525.png)

If you need to upload a PDF file, click on the Assets button to change the current directory to the `assets` folder inside your Foundry data directory.

![Pasted image 20260720130722.png](../images/Pasted%20image%2020260720130722.png)

Notice that once you are in the `assets` folder, the **Upload: Choose File** button is enabled.

From here, you can either drag a PDF file from your hard drive onto this dialog to automatically upload it and refresh the view, or click the Upload: Choose File button to manually navigate to the PDF file and select it.

![Pasted image 20260720131600.png](../images/Pasted%20image%2020260720131600.png)

### Update the Page Offset and Book Code

In the resulting PDF page editor, finish by entering the Page Offset and the PDF Book Code.

The **Page Offset** is a number that GGA will use to correctly set the page number when opening a PDF to a specific page. This is usually needed when the PDF document contains cover art or other pages before page numbering starts.

The **PDF Book Code** is what code you want to correspond to this PDF. For example, PDF Book Code "B" might mean the GURPS Basic PDF book.

In my example, I'm using "PY3/83" to mean Pyramid Issue 3/83, "Alternative GURPS IV".

The GURPS Character Sheet author maintains a list of [PDF Page Codes](https://gurpscharactersheet.com/page_references.html).

After you've set these values, click **Save Entry** and close this window.

## 3. Test the PDF

Enter the following command in the chat input area:

`[PDF:<code><page>]`

* Set `<code>` to the PDF Book Code you just defined.
* Set `<page>` to a page inside that PDF.

 > 
 > \[!NOTE\] NOTE
 > If the `<code>` ends in a number, you must put a colon (':') between the`<code>` and the `<page>`.

In my example, I might enter `[PDF:PY3/83:7]` — Open Pyramid 3/83 to page 7.

Hit the ENTER key. You will get a new chat message like this:
![Pasted image 20260720133121.png](../images/Pasted%20image%2020260720133121.png)

This is a link to the PDF that should open to the correct page if you click it. This is also how you might share a PDF link with other players in chat.

That same text (`[PDF:PY3/83:7]`) could be placed on a character sheet or a text journal page, and it will always be treated as a link to the PDF and page.

Most of the Character Sheets include PDF links to the source material that documents the Trait, Skill, Spell, or Equipment.
![Pasted image 20260720133329.png](../images/Pasted%20image%2020260720133329.png)
*Figure: The values in the Ref column are PDF links to the Dungeon Fantasy RPG Adventurers PDF. Note that no colon is needed as the book code "DFA" does not end in a number.*

## 4. Set Permissions

If you want other players to be able to open the PDF, go to the Journal Entry tab, and right-click on  the Journal Entry that contains your PDF. Select **Configure Ownership** and then select the **All Players** pulldown, pick **Observer** (they can read but not change the Journal Entry) and then click **Save Changes**.

NOTE: If you created multiple Journal Entries for your PDFs (instead of adding them as separate pages to the “PDF” journal entry), you will need to change the permission on ALL of the PDF Journal Entries.

An organizing principle therefore might be to collect all "public" PDFs in a single Journal Entry.

# About Basic: Campaigns and Basic: Characters

SJGames provides a unified single PDF that combines both the Characters and Campaign books into a single PDF, AND they provide these as separate PDFs. But when you see a PDF page reference, they are always treated as a single volume.

For example, B101 is a reference to Basic page 101 (Trait Modifiers) which is in the Characters book, while B400 (Grappling and Hit Locations) is a reference to page 400 in the Campaigns book.

If you have separate PDFs, set GURPS Basic Characters to PDF Book Code 'B' and Basic Campaigns to code 'BX', and use the [PDF Settings](Settings%20Subpages/Miscellaneous%20Settings.md#pdf-settings) in GGA to **Separate (Characters, B; Campaigns, BX)**.
