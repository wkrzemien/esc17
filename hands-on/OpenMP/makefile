#
#  USAGE:
#     make          ... to build the program
#     make test     ... to run the default test case
#

include make.def

EXES=hello$(EXE) pi$(EXE) mandel$(EXE) linked$(EXE) 

all: $(EXES)

hello$(EXE): hello.$(OBJ) 
	$(CLINKER) $(OPTFLAGS) -o hello hello.$(OBJ) $(LIBS)

pi$(EXE): pi.$(OBJ) 
	$(CLINKER) $(OPTFLAGS) -o pi pi.$(OBJ) $(LIBS)

pi_recur$(EXE): pi_recur.$(OBJ) 
	$(CLINKER) $(OPTFLAGS) -o pi_recur pi_recur.$(OBJ) $(LIBS)

mandel$(EXE):  mandel.$(OBJ) 
	$(CLINKER) $(OPTFLAGS) -o mandel mandel.$(OBJ) $(LIBS)

linked$(EXE):  linked.$(OBJ) 
	$(CLINKER) $(OPTFLAGS) -o linked linked.$(OBJ) $(LIBS)

racey$(EXE):  racey.$(OBJ) 
	$(CLINKER) $(OPTFLAGS) -o racey racey.$(OBJ) $(LIBS)

test: $(EXES)
	for i in $(EXES); do \
            $(PRE)$$i; \
        done

clean:
	$(RM) $(EXES) *.$(OBJ)

.SUFFIXES:
.SUFFIXES: .c .cpp .$(OBJ)

.c.$(OBJ):
	$(CC) $(CFLAGS) -c $<

.cpp.$(OBJ):
	$(CC) $(CFLAGS) -c $<
