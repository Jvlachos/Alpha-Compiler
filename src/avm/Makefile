CC = g++
CFLAGS = -Wall -ansi -pedantic -g -std=c++11
SAN = -fsanitize=address
avm: main/avm.o conversions/conversions.o exec/assignexec.o exec/functionexec.o exec/jumpexec.o exec/operationexec.o libfunctions/libfunctions.o exec/tableexec.o
	@$(CC) $(CFLAGS)  $^ -o $@
%.o: %.cpp
	@$(CC) $(CFLAGS) -o $@ -c $<


clean:
	@rm -f avm
	@rm -f main/*.o exec/*.o
	@rm -f conversions/*.o
