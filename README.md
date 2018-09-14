# teste
## Example CSV import. Use ## for comments and # for configuration. Paste CSV below.
## The following names are reserved and should not be used (or ignored):
## id, tooltip, placeholder(s), link and label (see below)
##
#
## Node label with placeholders and HTML.
## Default is '%name_of_first_column%'.
#
# label: %name%<br><i style="color:gray;">%position%</i><br>
#
## Node style (placeholders are replaced once).
## Default is the current style for nodes.
#
# style: label;image=%image%;whiteSpace=wrap;html=1;rounded=1;fillColor=%fill%;strokeColor=%stroke%;
#
## Parent style for nodes with child nodes (placeholders are replaced once).
#
# parentstyle: swimlane;whiteSpace=wrap;html=1;childLayout=stackLayout;horizontal=1;horizontalStack=0;resizeParent=1;resizeLast=0;collapsible=1;
#
## Uses the given column name as the identity for cells (updates existing cells).
## Default is no identity (empty value or -).
#
# identity: -
#
## Uses the given column name as the parent reference for cells. Default is no parent (empty or -).
## The identity above is used for resolving the reference so it must be specified.
#
# parent: -
#
## Adds a prefix to the identity of cells to make sure they do not collide with existing cells (whose
## IDs are numbers from 0..n, sometimes with a GUID prefix in the context of realtime collaboration).
## Default is csvimport-.
#
# namespace: csvimport-
#
## Connections between rows ("from": source colum, "to": target column).
## Label, style and invert are optional. Defaults are '', current style and false.
## In addition to label, an optional fromlabel and tolabel can be used to name the column
## that contains the text for the label in the edges source or target (invert ignored).
## The label is concatenated in the form fromlabel + label + tolabel if all are defined.
## The target column may contain a comma-separated list of values.
## Multiple connect entries are allowed.
#
# connect: {"from": "manager", "to": "name", "invert": true, "label": "", \
#          "style": "straight=1;endArrow=blockThin;endFill=1;fontSize=11;"}
# connect: {"from": "refs", "to": "id", "style": "curved=1;fontSize=11;"}
#
## Node x-coordinate. Possible value is a column name. Default is empty. Layouts will
## override this value.
#
# left: 
#
## Node y-coordinate. Possible value is a column name. Default is empty. Layouts will
## override this value.
#
# top: 
#
## Node width. Possible value is a number (in px), auto or an @ sign followed by a column
## name that contains the value for the width. Default is auto.
#
# width: auto
#
## Node height. Possible value is a number (in px), auto or an @ sign followed by a column
## name that contains the value for the height. Default is auto.
#
# height: auto
#
## Padding for autosize. Default is 0.
#
# padding: -12
#
## Comma-separated list of ignored columns for metadata. (These can be
## used for connections and styles but will not be added as metadata.)
#
# ignore: id,image,fill,stroke
#
## Column to be renamed to link attribute (used as link).
#
# link: url
#
## Spacing between nodes. Default is 40.
#
# nodespacing: 40
#
## Spacing between parallel edges. Default is 40.
#
# edgespacing: 40
#
## Name of layout. Possible values are auto, none, verticaltree, horizontaltree,
## verticalflow, horizontalflow, organic, circle. Default is auto.
#
# layout: verticaltree
#
## ---- CSV below this line. First line are column names. ----
name,position,id,location,manager,email,fill,stroke,refs,url,image
Diretor Informação Processos e Controle,CFO,emi,Office 1,,me@example.com,#dae8fc,#6c8ebf,,https://www.draw.io,https://cdn3.iconfinder.com/data/icons/user-avatars-1/512/users-9-2-128.png
Coordenador da Qualidade,Brand Manager,emo,Office 2,Diretor Informação Processos e Controle,me@example.com,#d5e8d4,#82b366,,https://www.draw.io,https://cdn3.iconfinder.com/data/icons/user-avatars-1/512/users-10-3-128.png
Gerente de Controladoria,System Admin,rdo,Office 3,Diretor Informação Processos e Controle,me@example.com,#d5e8d4,#82b366,,https://www.draw.io,https://cdn3.iconfinder.com/data/icons/user-avatars-1/512/users-2-128.png
Gerente de Auditoria,HR Director,tva,Office 4,Diretor Informação Processos e Controle,me@example.com,#d5e8d4,#82b366,,https://www.draw.io,https://cdn3.iconfinder.com/data/icons/user-avatars-1/512/users-3-128.png

Coordenador de Sistemas e TI,HR Director,tva,Office 4,Diretor Informação Processos e Controle,me@example.com,#d5e8d4,#82b366,,https://www.draw.io,https://cdn3.iconfinder.com/data/icons/user-avatars-1/512/users-3-128.png

Analista da Qualidade,System Admin1,rdo,Office 3,Coordenador da Qualidade,me@example.com,#d5e8d4,#82b366,,https://www.draw.io,https://cdn3.iconfinder.com/data/icons/user-avatars-1/512/users-2-128.png
Assistente da Qualidade,HR Director,tva,Office 4,Coordenador da Qualidade,me@example.com,#d5e8d4,#82b366,,https://www.draw.io,https://cdn3.iconfinder.com/data/icons/user-avatars-1/512/users-3-128.png
