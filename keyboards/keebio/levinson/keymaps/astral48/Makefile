# Helper makefile for misc utils.

flash: gensrcs
	echo "==== Flash A ===="
	qmk flash -kb keebio/levinson/rev3 -bl dfu
	echo
	echo
	echo "==== Flash B ====" 
	qmk flash -kb keebio/levinson/rev3 -bl dfu

gensrcs: json_generated.c

json_generated.c: astral48.json
	qmk json2c astral48.json -o json_generated.c

clean:
	rm json_generated.c
