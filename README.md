# Partops - Partitional Operators
Partitional Operators (Partops v. 1.35 Beta) is a tool for compositional or analytical tasks in Partitional Analysis. It is a program aimed at composers, music researchers, especially in texture and analysis, and those interested in better understanding Partitional Analysis and its derived theories. Version 1.35 Beta is in the testing phase and is offered as open-source software.

![image](https://github.com/Pauxygnunes/Partops/assets/30673056/1b0d4ec4-1662-4e2d-9072-bc78f91a2634)

# Basic Instructions
The interface of the Partops program consists of a table with time points (first column) and partitions (remaining columns, one part per column). The panels on the left can be understood as a calculator that applies partition operators to partitions, for selection and insertion into the table.
# Interface

![Partops Elements](https://github.com/Pauxygnunes/Partops/assets/30673056/a8c3128b-5d0a-4111-ac20-cda644093dff)

1. Table
By default, the table has 16 rows and 11 columns, but the program can load tables with other dimensions. The size can also be changed while working.
- To edit the cell values:
1. Click or double-click on any numeric value and type.
2. Alternatively, it is possible to insert the partition directly, using Selection and Control Panels (items 2 and 5).
3. Time points accept decimal values.
4. Partitions fields (parts) accept integer values only (the interface ignores decimal values).
- To add a new row to the table:
1. Select a row by clicking on a value or a cell.
2. Click the Dupl button, inside Control Panel (item 5). The selected line duplicate and its values are available for editing.
3. The selected line appears in the sel. row field, inside Control Panel (item 5).

![image](https://github.com/Pauxygnunes/Partops/assets/30673056/35b6897b-aa0e-4616-be8f-18e9e673f7ce)

- To delete a row, select a row by clicking on a value or a cell.
1. Click the Del button, inside Control Panel (item 5). The row goes away, and the interface rearranges the subsequent ones.
2. The selected row number appears in the sel. row field, inside Control Panel (item 5).
- To reset the table In the main menu, select Table> Reset. The table returns to the default state.
- To save the table In the main menu, select Table> Save or use the shortcut Ctrl+S
- To load a table previously saved or produced through the Parsemat program In the main menu, select Table> Open or use the shortcut Ctrl+O.
# Selection Panel
The Selection window shows the result of applying the partitional operators – resizing (m), revariance (v), and transfer (t) to the current partition. This window is not editable and only serves to monitor results and insert them into the table using the Ins button. When opening the program, the Selection window initializes with partition [1].

![image](https://github.com/Pauxygnunes/Partops/assets/30673056/3aeef8b1-d0ca-4a14-a40c-f2fa4327ba9c)

When the result of the application of the operator generates more than one partition, a list of partitions is displayed. The one selected is always the first in the list; to access the next ones, use the Rot button, inside Control Panel (item 5).
# Indices
This panel displays the indices of agglomeration (a), dispersion (d), and the global number of internal relations (T), referring to the partition in the Selection window.
- The agglomeration index (a) reflects the degree of dependence or internal convergence between components of the partition. Musically, this can mean more massive vertical situations, more dependent melodic lines, or more homogeneous instrumentations, and many other meanings, depending on the type of application.
- The dispersion index (d) indicates the degree of diversity or distinction between the internal components of the partition. Musically, this can mean explicit or implicit polyphonies (melodic), more colorful instruments, and many other meanings, depending on the type of application.
- The total index of relations (T) is the sum of the indexes (a, d). It corresponds to the number of total interactions between components involved in the integer partition, given by all pairwise combinations.
# Operators
Six basic operations are available, coming from Partitional Analysis: three operators, in positive and negative forms.
- Resizing (m): quantitative unitary change of one of the parts. Positive, when the part thickens (+ m). Negative, when the part tapers (-m).
- Revariance (v): addition (+ v) or subtraction (-v) of a unitary part to the integer partition.
- Transfer (t): when a unitary component is transferred from one part to another, unitary or not. This operation is composed, as it comprises two simple operations (m and/or v) with opposite signs ([+ m -v] or [-m + v]; in some cases, [+ m -m]). The transfer is positive (+t) when it causes progression (movement towards more dispersed partitions) and negative (-t) when it causes recession (movement towards more agglomerated partitions).
In some cases, the operation is not applicable (there are no results from the partition that is in the selection window). This is part of the background strucucture formed by the operators. When this happens, when you click the button, the selection window remains in the same state.
# Control
The buttons on this panel help to modify or select the data produced in the selection window and the table.
- CE – resets the selection window, returning to the default partition [1].
- Rot – in cases where the application of the operators results in two or more partitions, the Rot button allows the selection of each one, through the vertical rotation of the list of partitions.
- Del – delete a row from the table. Clicking on a value or cell selects the corresponding row. The sel. row field indicates line selection.
- Dupl – duplicates a row in the table. You must select a row by clicking on a value or cell in the table.

![image](https://github.com/Pauxygnunes/Partops/assets/30673056/5fa7dcbb-17d2-4e74-9564-4be1a96e3acd)

- ▲ (up) and ▼ (down) – allow navigation through the table rows. Navigation can also proceed by clicking on values or cells. Insertion also causes selection to proceed to next row.
- Ins – inserts the selection window partition into a row in the table. After insertion, the next row is selected. You must also select a row by clicking on a value or cell in the table. Up and down buttons are another way to get the desired position.
# Graphics
After completion of the partition table, the program allows visualization in the form of an Indexogram, Particiogram, and Tempartgram.

![image](https://github.com/Pauxygnunes/Partops/assets/30673056/c28c2d8e-0ba8-4cc8-aec7-5ca884ae98bf)

- Index – produces the indexogram for the table. The opened window can be resized and brings Matlab figure toolbar and commands for editing and viewing (see reference 🔗). Indexogram shows the indexes of agglomeration and dispersion in mirror structure departing from the median line, horizontal axis read as time points, forming textural curves that can be used in form analysis or to assess the textural progression of a piece or musica excerpt.
- Partic – produces the partitiogram referring to the table. The opened window can be resized and brings the Matlab figure toolbar and commands for editing and viewing (see reference 🔗). Partitiogram shows all partitions used in the table with their positions defined according to their degrees of homogeneity or internal diversity. It shows too the set of all available partitions for the specific medium (instrumental group, number of sound sources, melodic internal lines, timbres, for example). This allows the assessment of the amount of use of the global resources of the context in the piece as well as the poietic of the composer, and the comprehension of the trajectories of the musical discourse through time.
- Ptemp – produces the temporal partitiogram, which brings together the Index and Partic data in an integrated 3D graph, including the temporal domain. The figure can be rotated for a complete comprehension of the relations between indices, tempo, and positions of partitiogram. For a global understanding of the relationship between indexes, time, and positions of the partitiogram, you can rotate the figure. In the figure, the X-Y, X-Z, and Y-Z rotation options provide the indexogram, partitiogram, and the agglomeration and dispersion curves (clicking the rotation icon in the toolbar and right-click in the figure for accessing the rotation options).
In the three graphs, once the window is open, it is possible to edit the table and click again on the corresponding button to update the graph immediately, without having to close the figure. In the figure window menu, there are several options for viewing, annotating, editing and exporting graphics.
# References
For understanding the basic concepts of Partitional Analysis, we recommend the following bibliography:
[Partitional Analysis Publications]([url](https://pauxy.net/partitional-analysis-publications/))
# Download and Installation
# Version 1.35 Beta – What’s new
1. Interface revamped and optimized.
2. Partition tables can now be saved and loaded. This feature allows interaction with future versions of Parsemat software, expected to bring the same functionality.
3. The table have now editable cells and lines.
4. The table have now also editable time points.
5. The table is now flexible concerning selection, adding and deleting lines.
6. The inferface counts with a feedback about the selected line number, above table.
7. Rendering of partitiogram is revised and more stable.
8. Option added for temporal partitiogram (ptemp), which summarizes the data of the remaining graphs.
9. Control panel have now buttons for deleting (Del) and duplicating (Dupl) table lines.
10. Partitions can now be automatically added to the table through the Ins button.
11. Rotation of partitions lists through Rot button is revised and more stable.
12. Resetting of table and selection pane is available at any time.
13. Figures show now the full standard menu for Matlab figures.
14. Table is resized automatically when inserted partitions exceed the number of columns.
15. Application title was removed from the interface and inserted in the windows title bar.
# About
PARTOPS – Partitional Operators version 1.35 Beta. Copyright © 2020 by Pauxy Gentil Nunes Filho.
Developed by Pauxy Gentil Nunes Filho and Daniel Moreira de Sousa, pauxy.contact@gmail.com | danielspro@hotmail.com
The functions ‘onset’, ‘dur’ and ‘channel’ are part of MIDI Toolbox Software Package, by Tuomas Eerola & Petri Toiviainen, Department of Music, ptee@cc.jyu.fi, ptoiviai@cc.jyu.fi, Copyright © 2004, University of Jyvaskyla, Finland.

This program is free software; you can redistribute it and/or modify it under the terms of version 2 of GNU General Public License as published by the FreeSoftware Foundation.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. This is free software, and you are welcome to redistribute it under certain conditions. See the GNU General Public License for more details. You should have received a copy of the GNU General Public License along with this program; if not, write to the Free Software Foundation, Inc.,59 Temple Place – Suite 330,Boston, MA 02111-1307, USA.28.
