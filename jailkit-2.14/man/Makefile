INSTALL = /usr/bin/install -c
prefix = /usr
datadir = ${datarootdir}
datarootdir = ${prefix}/share
mandir = ${datarootdir}/man

SRCS = \
	jailkit.8 \
	jk_chrootsh.8 \
	jk_uchroot.8 \
	jk_lsh.8 \
	jk_socketd.8 \
	jk_init.8 \
	jk_check.8 \
	jk_cp.8 \
	jk_chrootlaunch.8 \
	jk_addjailuser.8 \
	jk_jailuser.8 \
	jk_list.8 \
	jk_update.8

#SRCS += jk_procmailwrapper.8

MANS = $(SRCS:.8=.8.gz)

#%.8.gz : %.8
#	gzip -9 > $@ < $<

#.in.default:
#all: ${SRCS}
#	for file in ${SRCS} ; do \
#		gzip < $${file} > $${file}.gz ;\
#	done

jailkit.8.gz: jailkit.8
	gzip -9 < jailkit.8 > $@

jk_chrootsh.8.gz: jk_chrootsh.8
	gzip -9 < jk_chrootsh.8 > $@

jk_uchroot.8.gz: jk_uchroot.8
	gzip -9 < jk_uchroot.8 > $@

jk_lsh.8.gz: jk_lsh.8
	gzip -9 < jk_lsh.8 > $@

jk_socketd.8.gz: jk_socketd.8
	gzip -9 < jk_socketd.8 > $@

jk_init.8.gz: jk_init.8
	gzip -9 < jk_init.8 > $@

jk_check.8.gz: jk_check.8
	gzip -9 < jk_check.8 > $@

jk_cp.8.gz: jk_cp.8
	gzip -9 < jk_cp.8 > $@

jk_chrootlaunch.8.gz: jk_chrootlaunch.8
	gzip -9 < jk_chrootlaunch.8 > $@

jk_procmailwrapper.8.gz: jk_procmailwrapper.8
	gzip -9 < jk_procmailwrapper.8 > $@

jk_jailuser.8.gz: jk_jailuser.8
	gzip -9 < jk_jailuser.8 > $@

jk_addjailuser.8.gz: jk_addjailuser.8
	gzip -9 < jk_addjailuser.8 > $@

jk_list.8.gz: jk_list.8
	gzip -9 < jk_list.8 > $@

jk_update.8.gz: jk_update.8
	gzip -9 < jk_update.8 > $@

jailkit: ${MANS}

all: jailkit
	
install: jailkit
	${INSTALL} -d -m 755 ${DESTDIR}${mandir}/man8/
	for file in ${MANS} ; do \
		${INSTALL} -m 0644 $${file} ${DESTDIR}${mandir}/man8/ ;\
	done

uninstall:
	for file in ${MANS} ; do \
		rm -f ${DESTDIR}${mandir}/man8/$${file} ;\
	done

clean:
	rm -f *.gz
	rm -f *~

distclean: clean
	rm -f Makefile
