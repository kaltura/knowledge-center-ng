---
layout: page
title: " How to search through categories in the KMC?"
date: 2013-06-16 23:27:25
---

## Categories Search Rules

When searching for categories from the KMC search box in the Cagtegories page, the following rules apply:

*   The Kaltura search engine will match the search term within the KMC search box against the following <a name="category_attributes"></a>category attributes:  
    Category Name, Category ID , Category Tags, Category's Description, Category Reference ID, or any Category custom data fields of type: text that was set to be searchable.
*   Search criteria may include alphanumeric  as well as special characters such as: `, ~, !, @, #, $, %, ^, &, *, (, ), -, _, =, +, [, ], {, }, ;, :, ', \, |, /, ?, <, >
*   The **space character** is treated as an AND search operand. For example, searching for” hello world” will result with all entries that include both the word hello and the word **world** in one of the searchable category attributes.
*   The** comma character** is treated as an OR search operand. For example, searching for **hello, world** will result with all entries that include either the word **hello**, or the word **world** in one of the searchable category attributes.
*   The **! character** is treated as an AND NOT search operand. For example, searching for **hello ! world** should result with all entries that include the word hello but do not include the word world. The ! at the beginning of the search criteria is not supported within this AND NOT operant context.  When searching for actual words that start/end with the ! character, the ! character should be escapes using a backslash. For example, if you want to search for categories that include the word** !hello** or **hello!**, enter the following terms within the KMC search box: **\!hello or hello\!**
*   The** “” characters** are treated as an EXACT MATCH search operand. For example, searching for **hello world** will result with all categories that include the exact **hello world **phrase in one of the searchable entry attributes.

When managing your categories, the search box in the Categories page enables you to search for specific categories or catagory attributes that exist in your account. 

<p class="mce-procedure">
  To search through categories
</p>

> 1.  <span style="font-size: small;"></span>Go to the Content tab and select the Categories tab.
> 2.  Enter your search criteria and click the magnifying icon on the right, or press Enter.   
>     The search is applied on the category or the [category attributes][1]. For canned lists use the Categories Metadata Filters.
>     
>     You can search for content and then create playlists containing the filtered content. 

 [1]: #category_attributes

<p class="Procedure mce-procedure">
  To clear the search box
</p>

*   Click the X icon on the right.

 

 

<span style="font-size: small;"> </span>