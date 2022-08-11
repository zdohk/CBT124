~~~~~~~~~~~~~~~~

//***FILE 124 IS FROM THE STATE OF WISCONSIN REGIONAL COMPUTING     *   FILE 124
//*           CENTER OF MADISON, WISCONSIN AND CONTAINS             *   FILE 124
//*           SEVERAL OF THEIR ISPF/PDF APPLICATIONS. THEY ARE      *   FILE 124
//*           CURRENTLY WORKING UNDER ISPF/PDF V2 R3 M0.            *   FILE 124
//*                                                                 *   FILE 124
//*           NO WARRANTY IS GIVEN OR IMPLIED BY WSRCC.             *   FILE 124
//*           NO LIABILITY IS ASSUMED BY WSRCC FOR ANY OF           *   FILE 124
//*           THE CODE IN THIS FILE.                                *   FILE 124
//*                                                                 *   FILE 124
//*           THIS FILE IS IN IEBUPDTE SYSIN FORMAT                 *   FILE 124
//*                                                                 *   FILE 124
//*           THIS FILE CONTAINS THE FOLLOWING MEMBERS :            *   FILE 124
//*                                                                 *   FILE 124
//*           AUTH        -  MACRO, USED BY SPF (SEE BELOW).  AUTH  *   FILE 124
//*                          IS USED BY THE SPF PROGRAM TO INVOKE   *   FILE 124
//*                          SVC 233 TO TURN ON AND OFF JSCB        *   FILE 124
//*                          AUTHORIZATION.                         *   FILE 124
//*                                                                 *   FILE 124
//*           BPPL        -  MACRO TAKEN FROM CBT TAPE VERSION 259  *   FILE 124
//*                          FILE 270.  USED IN ASSEMBLY OF STACK   *   FILE 124
//*                          PROGRAM.                               *   FILE 124
//*                                                                 *   FILE 124
//*           EDPRD       -  ISREDIT MACRO TO INVOKE THE PRINTDS    *   FILE 124
//*                          COMMAND FOR THE DATASET BEING EDITED.  *   FILE 124
//*                          USES THE PDPANL PANEL TO PROMPT FOR    *   FILE 124
//*                          OPTIONS WHICH ARE SAVED IN THE         *   FILE 124
//*                          PROFILE.  THE MACRO WORKS AGAINST THE  *   FILE 124
//*                          DISK VERSION OF THE DATASET SO IF      *   FILE 124
//*                          CHANGES HAVE BEEN MADE THE DATASET     *   FILE 124
//*                          MUST BE "SAVE"ED BEFORE INVOKING       *   FILE 124
//*                          EDPRD.                                 *   FILE 124
//*                                                                 *   FILE 124
//*           EDPRT       -  ISREDIT MACRO TO INVOKE THE PRINTOFF   *   FILE 124
//*                          COMMAND FOR THE DATASET BEING EDITED.  *   FILE 124
//*                          USES THE PRPANL PANEL TO PROMPT FOR    *   FILE 124
//*                          OPTIONS WHICH ARE SAVED IN THE         *   FILE 124
//*                          PROFILE.  THE MACRO WORKS AGAINST THE  *   FILE 124
//*                          DISK VERSION OF THE DATASET SO IF      *   FILE 124
//*                          CHANGES HAVE BEEN MADE THE DATASET     *   FILE 124
//*                          MUST BE "SAVE"ED BEFORE INVOKING       *   FILE 124
//*                          EDPRT.                                 *   FILE 124
//*                                                                 *   FILE 124
//*           EDSCR       -  ISREDIT MACRO TO INVOKE THE SCRIPT     *   FILE 124
//*                          COMMAND FOR THE DATASET BEING EDITED.  *   FILE 124
//*                          USES THE SCPANL PANEL TO PROMPT FOR    *   FILE 124
//*                          OPTIONS WHICH ARE SAVED IN THE         *   FILE 124
//*                          PROFILE.  THE MACRO WORKS AGAINST THE  *   FILE 124
//*                          DISK VERSION OF THE DATASET SO IF      *   FILE 124
//*                          CHANGES HAVE BEEN MADE THE DATASET     *   FILE 124
//*                          MUST BE "SAVE"ED BEFORE INVOKING       *   FILE 124
//*                          EDSCR.                                 *   FILE 124
//*                                                                 *   FILE 124
//*           ENTERR      -  MACRO TAKEN FROM CBT TAPE VERSION 259  *   FILE 124
//*                          FILE 270.  USED IN ASSEMBLY OF STACK   *   FILE 124
//*                          PROGRAM.                               *   FILE 124
//*                                                                 *   FILE 124
//*           GDGUTIL     -  ISPF CLIST WHICH INVOKES SEVERAL       *   FILE 124
//*                          FUNCTIONS ONE MIGHT WANT TO DO TO A    *   FILE 124
//*                          GDG.  CREATE, LIST INDEX, LIST         *   FILE 124
//*                          DATASETS MODIFY LIMIT AND DELETE.      *   FILE 124
//*                          CAN BE USED FROM PANEL 6 OR INCLUDED   *   FILE 124
//*                          AS A SELECTION ENTRY ON ANOTHER        *   FILE 124
//*                          PANEL.  USES GDGUTILP PANEL AND        *   FILE 124
//*                          RESETGDG PROGRAM TO DO THE WORK.       *   FILE 124
//*                                                                 *   FILE 124
//*           GDGUTILP    -  ISPF PANEL USED BY GDGUTIL, SEE ABOVE. *   FILE 124
//*                                                                 *   FILE 124
//*           IGC0023C    -  SVC 233.  THIS IS A NON-AUTHORIZED     *   FILE 124
//*                          TYPE 3 SVC THAT TURNS BITS IN THE      *   FILE 124
//*                          JSCB ON OR OFF BASED ON AN ENTRY       *   FILE 124
//*                          CODE IS REGISTER 1.  IT IS CALLED BY   *   FILE 124
//*                          THE AUTH MACRO WHICH IS USED BY THE    *   FILE 124
//*                          SPF PROGRAM (SEE BELOW).               *   FILE 124
//*                                                                 *   FILE 124
//*           IKJCVT      -  MACRO TAKEN FROM CBT TAPE VERSION 259  *   FILE 124
//*                          FILE 270.  USED IN ASSEMBLY OF STACK   *   FILE 124
//*                          PROGRAM.                               *   FILE 124
//*                                                                 *   FILE 124
//*           ISR=PDOC    -  ISPF/PDF PRIMARY OPTION PANEL          *   FILE 124
//*                          DOCUMENTAION.                          *   FILE 124
//*                                                                 *   FILE 124
//*           ISR=PRIM    -  ISPF/PDF PRIMARY OPTION PANEL AS USED  *   FILE 124
//*                          BY WSRCC.  SEE THE MEMBER ISR=PDOC FOR *   FILE 124
//*                          DESCRIPTION.                           *   FILE 124
//*                                                                 *   FILE 124
//*           KPPL        -  MACRO TAKEN FROM CBT TAPE VERSION 259  *   FILE 124
//*                          FILE 270.  USED IN ASSEMBLY OF STACK   *   FILE 124
//*                          PROGRAM.                               *   FILE 124
//*                                                                 *   FILE 124
//*           LEAVER      -  MACRO TAKEN FROM CBT TAPE VERSION 259  *   FILE 124
//*                          FILE 270.  USED IN ASSEMBLY OF STACK   *   FILE 124
//*                          PROGRAM.                               *   FILE 124
//*                                                                 *   FILE 124
//*           MOVE        -  MACRO TAKEN FROM CBT TAPE VERSION 259  *   FILE 124
//*                          FILE 270.  USED IN ASSEMBLY OF STACK   *   FILE 124
//*                          PROGRAM.                               *   FILE 124
//*                                                                 *   FILE 124
//*           PDPANL      -  PROMPTING PANEL FOR USE WITH EDPRD     *   FILE 124
//*                          MACRO.                                 *   FILE 124
//*                                                                 *   FILE 124
//*           PRPANL      -  PROMPTING PANEL FOR USE WITH EDPRT     *   FILE 124
//*                          MACRO.                                 *   FILE 124
//*                                                                 *   FILE 124
//*           PRT         -  3.4 PRINTOFF CLIST, SAME AS J.PRT,     *   FILE 124
//*                          ALSO MAIN MEMBER FOR ALIASES PR1 AND   *   FILE 124
//*                          PR2 3.4 PRINTOFF CLISTS.               *   FILE 124
//*                                                                 *   FILE 124
//*           PRTPNL00    -  MEMBERS SELECTION LIST PANEL USED BY   *   FILE 124
//*                          J.PRT, J.PR1, J.PR2, AND THE 3.4       *   FILE 124
//*                          CLISTS PRT, PR1, AND PR2.              *   FILE 124
//*                                                                 *   FILE 124
//*           PR1 (ALIAS) -  3.4 PRINTOFF CLIST, USES SAME OPTIONS  *   FILE 124
//*                          AS J.PR1                               *   FILE 124
//*                                                                 *   FILE 124
//*           PR2 (ALIAS) -  3.4 PRINTOFF CLIST, USES SAME OPTIONS  *   FILE 124
//*                          AS J.PR2                               *   FILE 124
//*                                                                 *   FILE 124
//*           REGEQU      -  MACRO TAKEN FROM CBT TAPE VERSION 259  *   FILE 124
//*                          FILE 270.  USED IN ASSEMBLY OF STACK   *   FILE 124
//*                          PROGRAM.                               *   FILE 124
//*                                                                 *   FILE 124
//*           RESETGDG    -  PROGRAM TO RESET THE LIMIT ON GDG'S.   *   FILE 124
//*                          SEE PROGRAM FOR ADDITIONAL             *   FILE 124
//*                          INFORMATION.  CALLED BY GDGUTIL CLIST. *   FILE 124
//*                                                                 *   FILE 124
//*           SCPANL      -  PROMPTING PANEL FOR USE WITH SCPRT     *   FILE 124
//*                          MACRO.                                 *   FILE 124
//*                                                                 *   FILE 124
//*           SPF         -  WSRCC'S PREPROCESSOR WHICH ALLOCATES   *   FILE 124
//*                          ISPF/PDF FILES AND INVOKES ISPF/PDF.   *   FILE 124
//*                                                                 *   FILE 124
//*           SPFDOC      -  DOCUMENTATION FOR WSRCC'S ISPF/PDF     *   FILE 124
//*                          PREPROCESSOR                           *   FILE 124
//*                                                                 *   FILE 124
//*           STACK       -  STACK PROGRAM AS TAKEN FROM CBT TAPE   *   FILE 124
//*                          259 FILE 270, USED FOR ISPF/PDF XL     *   FILE 124
//*                          (EXIT AND LOGOFF) AND XLN (EXIT AND    *   FILE 124
//*                          LOGON) OPTIONS.                        *   FILE 124
//*                                                                 *   FILE 124
//*           STACKDOC    -  STACK PROGRAM DOCUMENTATION, ALSO AS   *   FILE 124
//*                          TAKEN FROM CBT TAPE VERSION 259, FILE  *   FILE 124
//*                          270.                                   *   FILE 124
//*                                                                 *   FILE 124
//*           WPROFILE    -  SAMPLE MEMBER FOR USE BY WSRCC         *   FILE 124
//*                          ISPF/PDF PREPROCESSOR, ALLOCATES       *   FILE 124
//*                          ISPF/PDF FILES AS USED BY WSRCC        *   FILE 124
//*                          CUSTOMER RATHER THAN AS WSRCC SYSTEMS  *   FILE 124
//*                          PROGRAMMER.                            *   FILE 124
//*                                                                 *   FILE 124
//*           WSRCCEP1    -  THIS PANEL IS CALLED BY ALL OF THE J   *   FILE 124
//*                          COMMANDS (EXCEPT FOR SET), IT DECODES  *   FILE 124
//*                          THE COMMAND'S SELECTION CODE INTO A    *   FILE 124
//*                          FULL DATA SET NAME AND INVOKES THE     *   FILE 124
//*                          WSRCEPCL CLIST TO HANDLE THE REQUESTED *   FILE 124
//*                          COMMAND.                               *   FILE 124
//*                                                                 *   FILE 124
//*                          SEVERAL DATASETS AND SELECTION CODES   *   FILE 124
//*                          ARE CODED INTO THE WSRCCEP1 PANEL AND  *   FILE 124
//*                          DO NOT NEED TO BE ADDED TO EACH        *   FILE 124
//*                          INDIVIDUAL'S SELECTIONS, THEY ARE      *   FILE 124
//*                          FREQUENTLY USED PDS'S:                 *   FILE 124
//*                                                                 *   FILE 124
//*                             CODE         LIBRARY                *   FILE 124
//*                              S1        SYS1.PROCLIB             *   FILE 124
//*                              S2        SYS2.PROCLIB             *   FILE 124
//*                              PA        SYS1.PARMLIB             *   FILE 124
//*                              C2        SYS2.CLISTLIB            *   FILE 124
//*                              TSO       SYS2.TSOPROCS            *   FILE 124
//*                              STC       SYS2.STCPROCS            *   FILE 124
//*                                                                 *   FILE 124
//*           WSRCCLPN    - THIS PANEL IS THE J JUMP COMMAND        *   FILE 124
//*                         SELECTION PANEL.  ALL OF THE COMMAND    *   FILE 124
//*                         OPTIONS ARE ALSO ADDED TO THE ISR=PRIM  *   FILE 124
//*                         PRIMARY PANEL SO YOU DO NOT NEED TO     *   FILE 124
//*                         ENTER J IN FRONT OF EACH OPTION, THIS   *   FILE 124
//*                         PANEL IS MAINLY USED TO SHOW WHICH      *   FILE 124
//*                         FUNCTIONS WORK WITH THE DATA SET NAME   *   FILE 124
//*                         SELECTION CODES.                        *   FILE 124
//*                                                                 *   FILE 124
//*           WSRCEPCL    - THIS IS THE MAIN JUMP COMMAND CLIST.    *   FILE 124
//*                         THIS CLIST IS CALLED BY ALL OF THE J    *   FILE 124
//*                         PANEL OPTIONS (EXCEPT SET) AND IT       *   FILE 124
//*                         INVOKES ALL OF THE J PANEL COMMANDS.    *   FILE 124
//*                                                                 *   FILE 124
//*           WSRCESET    - SELECTION CODE AND DATA SET NAME        *   FILE 124
//*                         SETTING FOR J OPTIONS.  THIS PANEL IS   *   FILE 124
//*                         CALLED BY OPTION J.SET AND IT ALLOWS    *   FILE 124
//*                         YOU TO SET UP SELECTION CODES AND DATA  *   FILE 124
//*                         SET NAMES AND THE PRINTOFF OPTIONS FOR  *   FILE 124
//*                         PR1 AND PR2.                            *   FILE 124
//*                                                                 *   FILE 124
//*           WSRCMDS     - XSPLIT                                  *   FILE 124
//*                         THIS IS AN EXAMPLE OF THE ENTRY IN OUR  *   FILE 124
//*                         ISPCMDS WHICH ALLOWS US TO ENTER        *   FILE 124
//*                         XSPLIT (ABRV. XS) ON ANY COMMAND LINE   *   FILE 124
//*                         AND BRING UP A NEW PRIMARY OPTION       *   FILE 124
//*                         PANEL (ISR=PRIM) ON TOP OF THE CURRENT  *   FILE 124
//*                         ISPF/PDF SCREEN.  YOU CAN THEN DO ANY   *   FILE 124
//*                         ISPF/PDF (ALMOST) OPTIONS AND WHEN YOU  *   FILE 124
//*                         ARE THROUGH YOU ENTER =X AND GO BACK    *   FILE 124
//*                         TO THE SCREEN YOU ENTERED THE XSPLIT    *   FILE 124
//*                         ON.  THIS WORKS SORT OF LIKE AN EXTRA   *   FILE 124
//*                         SPLIT, BUT YOU STILL ONLY HAVE 2        *   FILE 124
//*                         SCREENS TO SWAP BETWEEN.                *   FILE 124
//*                                                                 *   FILE 124
//*           WSRCPRTC    - PDS MEMBER LIST, SELECT, AND PRINTOFF   *   FILE 124
//*                         CLIST.  THIS CLIST IS USED BY OTHER     *   FILE 124
//*                         CLISTS (WSRCEPCL, PRT, AND PRT'S        *   FILE 124
//*                         ALIASES) TO DISPLAY A PDS MEMBER        *   FILE 124
//*                         SELECTION LIST AND THEN PRINTOFF EACH   *   FILE 124
//*                         OF THE MEMBERS SELECTED.                *   FILE 124
//*                                                                 *   FILE 124
//*           TP          - MACRO TAKEN FROM CBT TAPE VERSION 259   *   FILE 124
//*                         FILE 270.  USED IN ASSEMBLY OF STACK    *   FILE 124
//*                         PROGRAM.                                *   FILE 124
//*                                                                 *   FILE 124
//*           XABGN       - MACRO, USED BY SPF PROGRAM TO SET UP    *   FILE 124
//*                         STANDARD LINKAGE AT THE BEGINNING OF    *   FILE 124
//*                         THE PROGRAM.                            *   FILE 124
//*                                                                 *   FILE 124
//*           XAFIN       - MACRO, USED BY SPF PROGRAM TO EXIT AND  *   FILE 124
//*                         FREE UP WORK AREA GETMAINED BY XABGN.   *   FILE 124
//*                                                                 *   FILE 124
//*           XL          - EXIT ISPF AND LOGOFF CLIST              *   FILE 124
//*                         THIS SMALL CLIST ISSUES THE STACK       *   FILE 124
//*                         COMMAND TO STACK A LOGOFF COMMAND, IT   *   FILE 124
//*                         IS CALLED BY OPTION XL IN ISR=PRIM.     *   FILE 124
//*                                                                 *   FILE 124
//*           XLN         - EXIT ISPF AND LOGON CLIST               *   FILE 124
//*                         THIS SMALL CLIST ISSUES THE STACK       *   FILE 124
//*                         COMMAND TO STACK A LOGON COMMAND, IT    *   FILE 124
//*                         IS CALLED BY OPTION XLN IN ISR=PRIM.    *   FILE 124
//*                         THE CLIST DOES A VGET FOR 2 VARIABLES,  *   FILE 124
//*                         XT1 AND XT2.  X1 IS THE LOGON-ID TO BE  *   FILE 124
//*                         LOGGED ON AND XT2 (IF SPECIFIED) IS AN  *   FILE 124
//*                         ALTERNATE LOGON PROC TO BE USED.        *   FILE 124
//*                                                                 *   FILE 124
~~~~~~~~~~~~~~~~

