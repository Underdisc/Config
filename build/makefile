#=COLOUR========================================================================

#-TEXT--------------------------------------------------------------------------
RT=@tput setaf 1
GT=@tput setaf 2
YT=@tput setaf 3
BT=@tput setaf 4
PT=@tput setaf 5
CT=@tput setaf 6
WT=@tput setaf 7

#-BACKGROUND--------------------------------------------------------------------
RB=@tput setab 1
GB=@tput setab 2
YB=@tput setab 3
BB=@tput setab 4
PB=@tput setab 5
CB=@tput setab 6
WB=@tput setab 7

#-STYLE-------------------------------------------------------------------------
BOLD=@tput bold
UNDERLINE=@tput smul

#-RESET-------------------------------------------------------------------------
RESET=@tput sgr0

#=MACROS========================================================================

CC = clang++
CFLAGS = -c -O -Wall -Wextra -ansi -pedantic -Wunused -Werror

SRCDIR = ../Source/

OBJS = main.o Service.o Account.o Vault.o PrintUtils.o
EXE = key

#=TARGETS=======================================================================

$(EXE) : $(OBJS)
	$(GT)
	$(BOLD)
	$(CC) $(OBJS) -o $(EXE)
	$(RESET)


%.o : $(SRCDIR)%.cpp
	$(BT)
	$(BOLD)
	$(CC) $(CFLAGS) $< -o $@
	$(RESET)

clean :
	$(RT)
	rm $(EXE) $(OBJS)
	$(RESET)
