# merge_mind

Processes a Freemind mindmap file, replacing nodes linked to external files with the content of
those files


## Use-cases

### Single-sourcing documents / designs / project files

It's possible to write documents entirely in freemind, and then export them to OpenOffice, HTML,
etc.

With this tool and Freeminds' linking feature, you can share common content (for example,
legal disclaimers, "About the author" sections, tutorials, definitions, common web-pages (say,
contact pages) across multiple sites and documents, etc.

It may be especially handy for various documents ABOUT your sites / projects.  For example,
external/customer-level design specifications and internal/developer-level technical
specifications can both share content using this tool.

### Others?

If you're using this tool for anything else, please fire me off an email and let me know.  That
way, I can be inspired to work on it more, and can also bear your use cases in mind during
future changes.


## Requirements

python3
python3-lxml


## Usage

Let's say you have the following files:

	CommonNodes.mm
	MainFile.mm

and let's say that MainFile has a node which links to the CommonNodes.mm file.


Then running:

	merge_mind Mainfile.mm > MergedFile.mm

Will create a file containing combined node tree, with nodes from both files.

In the merged file, the id of the linked node will become the id of the top-level node in the
linked file.



## To do

It would probably make sense to support linking to sub-nodes within the linked file, as documented here:

	http://freemind.sourceforge.net/wiki/index.php/FreeMind_0.9.0:_The_New_Features#Linking_to_nodes_in_another_mm-file

This is kind of a half-baked feature in Freemind right now though, since you have to manually enter the
node id into the link path.

For my (current) purposes (single-sourcing documents with chapters elsewhere), linking to the top-level
node in the linked file gets the job done.


## License

Affero GPL, version 3.0 or higher


## Contact

Lee Braiden <leebraid@gmail.com>

