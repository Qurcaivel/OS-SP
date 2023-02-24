CC=gcc
CFLAGS=-W -Wall -Wno-unused-parameter -Wno-unused-variable -std=c11 -pedantic
LDFLAGS=

SRC=main.c
OBJ=$(SRC:.c=.o)
EXE=dirwalk

.PHONY: build exec run clean

run: build exec clean 

exec: 
	@echo "Running $(EXE)..."
	./$(EXE);

build: $(SRC) $(EXE)
	
$(EXE): $(OBJ) 
	$(CC) $(LDFLAGS) $(OBJ) -o $@

.cpp.o:
	$(CC) $(CFLAGS) $< -o $@

clean:
	rm -r $(EXE) $(OBJ)