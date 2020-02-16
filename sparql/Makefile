CODEFILES: \
 $(shell groovy ../findScripts.groovy .. .out | sort | uniq)

RQFILES: \
 $(shell groovy ../findScripts.groovy .. .rq | sort | uniq)

.PRECIOUS: %.java %.groovy

all: allScriptsCompiled

distclean: clean
	@rm -f *.md *.out

clean:
	@rm -f *~ allScriptsCompiled

allScriptsCompiled: ${RQFILES} ${CODEFILES}
	@touch allScriptsCompiled

%.rq: %.i.rq
	@echo "creating $@ ..."
	@groovy rqprocess $< > $@

%.out: %.rq md.*.template preprocess postprocess
	@echo "doing $@ ..."
	@groovy preprocess $< > $@
	@groovy postprocess $<
