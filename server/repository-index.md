# Repository Index



<figure><img src="../.gitbook/assets/index-file.png" alt="" width="375"><figcaption><p>Repository Manager Index</p></figcaption></figure>

Indexing is a central aspect of the Repository Manager server.

The role of the repository indexing process is to perform the heavy and long process of collecting and processing all information about a given repository and storing it in a nicely formatted and properly accessible file called the repository index file, alongside files relevant to applications, so that the information contained in them can be accessed instantly and frequently when needed.

The repository indexing process usually runs once per day in order to accomodate potential application updates, and always pulls latest changes from version control before it can start.

All files relevant to the repository index are contained in a "data" directory in the server's root, with the "index file" called index.json, located inside of the "data" directory.

If the index file happens to be missing/corrupt when required, an empty index will be generated and running an index will be required for repository information to be available.

The index is never directly exposed to the user, and is only used internally. The only way to access the contents of the index externally is through the [API](broken-reference).

## index.json

Below is a tree of the index file structure:

* {}
  * {} repository
    * name
    * provider
    * description
  * \[] categories
    * {} \<category objects>
      * name
      * display\_name
      * singular
      * plural
  * \[] contents
    * {} \<application objects>
      * [{} information](../manifests/essential-information/)
        * \<contents of manifest>
      * [{} source](../manifests/source/)
        * \<contents of manifest>
      * [{} treatments](../manifests/treatments/)
        * \<contents of manifest>
      * {} metaxml
        * {} app
          * \<contents of meta.xml in JSON>
      * {} index\_computed\_info
        * package\_type (dol/elf/thm)
        * md5\_hash
        * release\_date (int, unix epoch)
        * icon\_size (int)
        * compressed\_size (int)
        * binary\_size (int)
        * uncompressed\_size (int)
        * peripherals (in HBB-compatible format)
        * \[] subdirectories
