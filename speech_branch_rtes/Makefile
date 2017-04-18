INCLUDE_DIRS = 
LIB_DIRS = 
CC=gcc

CDEFS=
CFLAGS= -O0 -g $(INCLUDE_DIRS) $(CDEFS) 
LIBS= -DMODELDIR=\"`pkg-config --variable=modeldir pocketsphinx`\" `pkg-config --cflags --libs pocketsphinx sphinxbase`

HFILES= 
CFILES= speech_rec.c

SRCS= ${HFILES} ${CFILES}
OBJS= ${CFILES:.c=.o}

all:	speech_rec

clean:
	-rm -f *.o *.d
	-rm -f speech_rec

speech_rec: speech_rec.o
	$(CC) $(LDFLAGS) $(CFLAGS) -o $@ $@.o -lm $(LIBS)

depend:
	
.c.o:
	$(CC) $(CFLAGS) -c $< $(LIBS)

