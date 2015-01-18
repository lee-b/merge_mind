# merge_mind

Processes a Freemind mindmap file, replacing nodes linked to external files with the content of
those files


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

It would probably make sense to support linking to sub-nodes within the linked file.  For my
purposes (single-sourcing documents), linking to the top-level node in the linked file gets
the job done.


## License

Affero GPL, version 3.0 or higher


## Contact

Lee Braiden <leebraid@gmail.com>

