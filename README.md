# CBT103
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 103 CONTAINS ISPF/DIALOGS FROM MR WILLIAM R HORTON OF     *   FILE 103
//*           EASTMAN CHEMICAL COMPANY OF KINGSPORT, TN, WHICH      *   FILE 103
//*           CONTAINS A COPY OF THEIR ISPF CONSOLE DIALOG AND      *   FILE 103
//*           GRS/ENQ DIALOG.  SEE THE MEMBER CALLED $INSTALL FOR   *   FILE 103
//*           COMPREHENSIVE DOCUMENTATION PLUS INSTALLATION         *   FILE 103
//*           INSTRUCTIONS.  THIS FILE IS IN IEBUPDTE SYSIN FORMAT. *   FILE 103
//*                                                                 *   FILE 103
//*           BILL HORTON                                           *   FILE 103
//*           EASTMAN CHEMICAL COMPANY                              *   FILE 103
//*           BUILDING 284                                          *   FILE 103
//*           KINGSPORT, TENNESSEE 37662                            *   FILE 103
//*           PHONE (423) 229-3388  FAX (423) 229-3254              *   FILE 103
//*           IBMMAIL: USECHV58 (OV/VM), USECHU6L (TSO/MVS)         *   FILE 103
//*                                                                 *   FILE 103
//*    email address:  bhorton@cs.utk.edu                           *   FILE 103
//*                    bhorton@eastman.com                          *   FILE 103
//*                                                                 *   FILE 103
//*           THIS  FILE  CONTAINS  SAMPLE ISPF DIALOGS AND EDIT    *   FILE 103
//*           MACROS DEVELOPED AT TENNESSEE EASTMAN COMPANY.        *   FILE 103
//*           NO GUARANTEES  ARE MADE AS TO THE ACCURACY,           *   FILE 103
//*           SUITABILITY FOR YOUR INSTALLATION, ORIGINALITY,       *   FILE 103
//*           NOVELTY, OR CLEVERNESS OF ANY OF  THE  PANELS,        *   FILE 103
//*           CLISTS, OR PROGRAMS CONTAINED HEREIN.                 *   FILE 103
//*                                                                 *   FILE 103
//*           HERE ARE THE DESCRIPTIONS OF THE VARIOUS DIALOGS      *   FILE 103
//*           CONTAINED IN THIS FILE:  (UPDATED FOR OS/390 - 01-98) *   FILE 103
//*                                                                 *   FILE 103
//*           BROADCAST DATASET DIALOG                              *   FILE 103
//*                                                                 *   FILE 103
//*           THIS IS A DIALOG WHICH CAN BE USED TO KEEP            *   FILE 103
//*           TRACK OF UPDATES TO THE TSO BROADCAST DATASET.        *   FILE 103
//*           IT STORES INFORMATION ABOUT EACH MESSAGE IN           *   FILE 103
//*           AN ISPF TABLE, AND STORES EACH BROADCAST              *   FILE 103
//*           MESSAGE AS A PDS MEMBER.  MESSAGES CAN BE             *   FILE 103
//*           ADDED, MODIFIED, OR DELETED;  ENTRY AND UPDATE        *   FILE 103
//*           OF MESSAGES IS VIA ISPF EDIT.  MESSAGES ARE           *   FILE 103
//*           GIVEN AN EXPIRATION DATE AND WILL BE REMOVED          *   FILE 103
//*           FROM THE BROADCAST DATASET THE NEXT TIME THE          *   FILE 103
//*           DIALOG IS INVOKED (AND A BROADCAST MESSAGE IS         *   FILE 103
//*           CHANGED) AFTER THE EXPIRATION DATE.                   *   FILE 103
//*                                                                 *   FILE 103
//*           ISPF TABLE EDIT DIALOG                                *   FILE 103
//*                                                                 *   FILE 103
//*           THIS DIALOG CAN BE USED TO EDIT A COMMAND             *   FILE 103
//*           TABLE, INCLUDING ISRCMDS AND ISPCMDS.  THIS IS        *   FILE 103
//*           DONE BY COPYING THE TABLE TO THE USER'S PROFILE       *   FILE 103
//*           DATASET (ASSUMED TO BE ALLOCATED TO DDNAME            *   FILE 103
//*           ISPTABL) AND INVOKING THE ISPF COMMAND TABLE          *   FILE 103
//*           EDIT PROGRAM, ISPUCM, AGAINST IT.  IF THE TABLE       *   FILE 103
//*           IS CHANGED BY ISPUCM, THEN IT IS COPIED BACK TO       *   FILE 103
//*           ITS SOURCE.  ISPF MUST BE RECYCLED TO SEE THE         *   FILE 103
//*           EFFECTS OF THE CHANGE.                                *   FILE 103
//*                                                                 *   FILE 103
//*           CONSOLE DISPLAY FACILITY (CDF)                        *   FILE 103
//*                                                                 *   FILE 103
//*           THIS IS AN ISPF DIALOG TO DISPLAY MVS CONSOLE         *   FILE 103
//*           INFORMATION (AS IN SPY).  IF THE INVOKER IS           *   FILE 103
//*           AUTHORIZED (HAS OPER AUTHORITY), THEN MVS             *   FILE 103
//*           COMMANDS MAY ALSO BE ENTERED.  I DIDN'T WRITE         *   FILE 103
//*           THIS MYSELF.  I GOT IT FROM A MODS TAPE               *   FILE 103
//*           (PROBABLY THE CBT TAPE) AND MODIFIED IT               *   FILE 103
//*           FOR EXTENDED DATA STREAM CONSOLES (E.G., 3290S        *   FILE 103
//*           AND 3179S) AND FOR MVS SP 2.2.0.  THERE ARE A         *   FILE 103
//*           LOT OF WAYS TO ENTER MVS COMMANDS AND GET             *   FILE 103
//*           RESPONSES NOWADAYS, BUT WE STILL LIKE THIS            *   FILE 103
//*           WAY BEST.  THIS CODE WORKS WITH MVS/SP 3.1.0E         *   FILE 103
//*           (MVS/ESA).                                            *   FILE 103
//*                                                                 *   FILE 103
//*           GRS/ENQ DIALOG                                        *   FILE 103
//*                                                                 *   FILE 103
//*           THIS DIALOG DISPLAYS ENQUEUE INFORMATION.  YOU        *   FILE 103
//*           CAN REQUEST THAT ONLY CONTENTION INFORMATION          *   FILE 103
//*           BE DISPLAYED, OR YOU CAN SPECIFY JOBNAME, QNAME,      *   FILE 103
//*           AND / OR RNAME.  THIS IS CODE I GOT SOMEWHERE         *   FILE 103
//*           ELSE AND ADDED ISPF AROUND IT.                        *   FILE 103
//*                                                                 *   FILE 103
//*           PC3270 FILE TRANSFER DIALOG.                          *   FILE 103
//*                                                                 *   FILE 103
//*           THIS DIALOG IS MOSTLY JUST A PANEL WHICH              *   FILE 103
//*           FACILITATES THE USE OF THE PC3270 FILE                *   FILE 103
//*           TRANSFER PROGRAM WHILE IN ISPF.  THE PANEL HAS        *   FILE 103
//*           TUTORIAL PANELS WHICH GIVE SYNTAX AND SAMPLES         *   FILE 103
//*           FOR THE PC SEND AND RECEIVE COMMANDS.                 *   FILE 103
//*                                                                 *   FILE 103
//*           THE DIALOG IS INVOKED BY ENTERING "PC" ON THE         *   FILE 103
//*           COMMAND LINE OF THE BOTTOM PANEL OF ISPF.  A          *   FILE 103
//*           COMMAND TABLE ENTRY CAUSES THE CLIST VPCC TO          *   FILE 103
//*           BE INVOKED.  THIS CLIST DISPLAYS PANEL VPC WHICH      *   FILE 103
//*           PUTS THE COMMAND LINE AT THE BOTTOM                   *   FILE 103
//*           (REQUIRED BY IND$FILE).  THE USER CAN NOW ENTER       *   FILE 103
//*           THE SEND OR RECEIVE COMMAND ON HIS DOS SCREEN.        *   FILE 103
//*                                                                 *   FILE 103
//*           WHEN  THE FILE TRANSFER PROGRAM ENTERS "IND$FILE      *   FILE 103
//*           ..." ON THE ISPF THE COMMAND LINE, A COMMAND          *   FILE 103
//*           TABLE ENTRY INVOKES A CLIST (VPCTRAN)  WHICH          *   FILE 103
//*           ACTUALLY  INVOKES  THE  IND$FILE  COMMAND.            *   FILE 103
//*           VPCTRAN IS BASED ON ADMUPCFT FROM IBM VIA GDDM.       *   FILE 103
//*                                                                 *   FILE 103
//*           DIALOG TO DISPLAY LOGO OF SUBMITTER                   *   FILE 103
//*                                                                 *   FILE 103
//*           THIS  PROGRAM  DISPLAYS  THE  LOGO OF THE             *   FILE 103
//*           SUBMITTER OF THESE MODS ON AN ISPF PANEL.  IT         *   FILE 103
//*           MAY BE INVOKED VIA COMMAND  TABLE ENTRY LOGO.         *   FILE 103
//*           NOTE THAT ENTERING "LOGO DEBUG" WILL CAUSE SOME       *   FILE 103
//*           PROGRAM  VARIABLES  TO BE WRITTEN TO SYSPRINT,        *   FILE 103
//*           AND WILL DISPLAY SOME OF THE ARCS USED TO DRAW        *   FILE 103
//*           THE LOGO.                                             *   FILE 103
//*                                                                 *   FILE 103
//*           EXIT DIALOG                                           *   FILE 103
//*                                                                 *   FILE 103
//*           THIS  DIALOG  WILL  END  THE  ISPF  SESSION (IF       *   FILE 103
//*           NOT IN SPLIT SCREEN), AND (OPTIONALLY) LOG THE        *   FILE 103
//*           USER OFF TSO, AND LOG  ANOTHER USER  ON TSO.          *   FILE 103
//*           IT IS INVOKED BY ENTERING "EXIT" FROM ANY ISPF        *   FILE 103
//*           COMMAND LINE TO TERMINATE ISPF (GO TO  TSO            *   FILE 103
//*           READY), ENTERING  "LOGOFF"  TO  TERMINATE  ISPF       *   FILE 103
//*           AND LOG THE USER OFF TSO, OR "LOGON" TO               *   FILE 103
//*           TERMINATE ISPF, LOG THE USER OFF TSO, AND LOG         *   FILE 103
//*           ANOTHER USER ON TSO (THIS IS CONSIDERABLY             *   FILE 103
//*           QUICKER  THAN LOGGING COMPLETELY OFF THEN             *   FILE 103
//*           LOGGING BACK ON).                                     *   FILE 103
//*                                                                 *   FILE 103
//*           PC3270 SCREEN COPY EDIT MACRO (COPYSCRN)              *   FILE 103
//*                                                                 *   FILE 103
//*           THIS  MACRO FACILITATES THE ENTRY OF DATA INTO        *   FILE 103
//*           ISPF EDIT VIA THE WORK STATION CONTROL COPY           *   FILE 103
//*           FUNCTION OF PC 3270S.  IT PRESENTS A PANEL INTO       *   FILE 103
//*           WHICH  UP  TO  80  BYTE  RECORDS  MAY  BE             *   FILE 103
//*           COPIED.    AFTER THE DATA IS COPIED ONTO THE          *   FILE 103
//*           PANEL, PRESSING THE ENTER KEY ADDS THE DATA TO        *   FILE 103
//*           THE END OF THE  CURRENT  EDIT SESSION DATA AND        *   FILE 103
//*           CLEARS THE COPY PANEL TO ACCEPT MORE INPUT.           *   FILE 103
//*                                                                 *   FILE 103
//*           ELIST EDIT MACRO                                      *   FILE 103
//*                                                                 *   FILE 103
//*           ELIST IS A MACRO WHICH CAN BE USED TO LIST THE        *   FILE 103
//*           DATA CURRENTLY BEING EDITED VIA ISPF EDIT,            *   FILE 103
//*           INCLUDING CHANGES WHICH HAVE BEEN MADE, WITHOUT       *   FILE 103
//*           HAVING TO LEAVE EDIT OR SAVE THE DATA.  SYNTAX IS:    *   FILE 103
//*                                                                 *   FILE 103
//*             ELIST ATTR                                          *   FILE 103
//*                                                                 *   FILE 103
//*           WHERE "ATTR" IS ANY VALID SYSOUT ATTRIBUTE WHICH      *   FILE 103
//*           CAN BE SPECIFIED WITH THE TSO ALLOCATE COMMAND.       *   FILE 103
//*           EXAMPLES:                                             *   FILE 103
//*                                                                 *   FILE 103
//*         ELIST DEST(NYC.RMT21)  LIST ON AN RJE PRINTER ON        *   FILE 103
//*                                ANOTHER NODE                     *   FILE 103
//*         ELIST DEST(VM1.USER66) SEND TO A VM USER'S VIRTUAL      *   FILE 103
//*                                READER                           *   FILE 103
//*         ELIST CHARS(GT12)      LIST ON 3800                     *   FILE 103
//*                                                                 *   FILE 103
//*           IF NO ATTRIBUTE IS ENTERED, THE DEFAULT               *   FILE 103
//*           DESTINATION  OF  THE TSO USER'S SESSION WILL BE       *   FILE 103
//*           USED.                                                 *   FILE 103
//*                                                                 *   FILE 103
//*           INFO EDIT MACRO                                       *   FILE 103
//*                                                                 *   FILE 103
//*           THE INFO MACRO GETS INFORMATION ABOUT THE             *   FILE 103
//*           DATASET AND MEMBER BEING  EDITED,  AND DISPLAYS       *   FILE 103
//*           IT IN THE DATA VIA MSG AND NOTE LINES.   THE          *   FILE 103
//*           INFORMATION WILL  NOT  BE  SAVED,  AND  MAY  BE       *   FILE 103
//*           CLEARED VIA THE RESET COMMAND.                        *   FILE 103
//*                                                                 *   FILE 103
//*           SPELL EDIT MACRO                                      *   FILE 103
//*                                                                 *   FILE 103
//*           SPELL    INVOKES   IBM'S   DOCUMENT                   *   FILE 103
//*           COMPOSITION   FACILITY (SCRIPT/VS) TO CHECK           *   FILE 103
//*           SPELLING OF THE  DATA  CURRENTLY  BEING EDITED.       *   FILE 103
//*           LINES CONTAINING MISSPELLED WORDS HAVE A NOTE         *   FILE 103
//*           LINE INSERTED AFTER THEM, LISTING THE MISSPELLED      *   FILE 103
//*           WORDS  FOR  THE LINE.                                 *   FILE 103
//*                                                                 *   FILE 103
//*           ISPF SUPPORT FOR THE QUEUE COMMAND                    *   FILE 103
//*                                                                 *   FILE 103
//*           THIS  IS  AN UPDATE TO THE JES2 2.2.0 LEVEL OF        *   FILE 103
//*           QUEUE TO PROVIDE RUDIMENTARY ISPF SUPPORT.  THE       *   FILE 103
//*           RESULT IS NOT VERY  ELEGANT BUT THE MODS TO           *   FILE 103
//*           QUEUE ARE SMALL SO THAT THE CODE CAN BE REWORKED      *   FILE 103
//*           EASILY  FOR NEW VERSIONS OF QUEUE.  DETAILS ARE       *   FILE 103
//*           IN MEMBER $$ISPF.  THE QUEUE COMMAND ITSELF  IS       *   FILE 103
//*           NOT  CONTAINED HERE, JUST THE MODULES WHICH HAVE      *   FILE 103
//*           CHANGES FOR ISPF SUPPORT.                             *   FILE 103
//*                                                                 *   FILE 103
//*           TSO/E RACF CONVERSION AID                             *   FILE 103
//*                                                                 *   FILE 103
//*           THIS PROGRAM CAN BE USED, WHEN CONVERTING TSO         *   FILE 103
//*           LOGON INFORMATION FROM  SYS1.UADS TO RACF, TO         *   FILE 103
//*           MIGRATE THE FIRST TSO COMMAND TO BE ISSUED FROM       *   FILE 103
//*           SYS1.UADS TO RACF (WHICH IS NOT  DONE BY THE          *   FILE 103
//*           RACONVRT COMMAND).                                    *   FILE 103
//*                                                                 *   FILE 103
//*           INPUT  IS  A  FLAT  FILE OF 172 BYTE SYS1.UADS        *   FILE 103
//*           RECORDS.  YOU SHOULD CONCATENATE ALL SYS1.UADS        *   FILE 103
//*           MEMBERS TO PROVIDE THIS INPUT PUT.                    *   FILE 103
//*                                                                 *   FILE 103
//*           WHEN THE PROGRAM FINDS A TSO COMMAND TO BE            *   FILE 103
//*           ISSUED,  IT  UPDATES THE  APPROPRIATE FIELD IN        *   FILE 103
//*           THE RACF DATA BASE, SO THAT THIS COMMAND WILL         *   FILE 103
//*           NOT BE LOST  ACROSS  THE  CONVERSION  FROM            *   FILE 103
//*           SYS1.UADS TO RACF.                                    *   FILE 103
//*                                                                 *   FILE 103
//*           TSO LOGON UPDATE DIALOG                               *   FILE 103
//*                                                                 *   FILE 103
//*           THIS IS AN ISPF DIALOG TO FACILITATE THE              *   FILE 103
//*           UPDATING OF CERTAIN TSO  LOGON  INFORMATION           *   FILE 103
//*           FIELDS.  SOME OF THESE FIELDS CAN BE UPDATED          *   FILE 103
//*           FROM THE TSO/E FULLSCREEN LOGON PANEL, BUT  MANY      *   FILE 103
//*           OF OUR  TSO  USERS NEVER SEE THIS PANEL, AS WE        *   FILE 103
//*           HAVE A WINDOWING PACKAGE WHICH AUTOMATICALLY          *   FILE 103
//*           SUPPLIES THEIR PASSWORD.   ALSO, IT'S  MORE           *   FILE 103
//*           CONVENIENT TO CHANGE THESE FIELDS WHEN YOU THINK      *   FILE 103
//*           OF IT, RATHER THAN HAVING TO WAIT UNTIL YOUR          *   FILE 103
//*           NEXT LOGON.                                           *   FILE 103
//*                                                                 *   FILE 103
//*           INFORMATION WHICH MAY BE UPDATED IN THIS DIALOG       *   FILE 103
//*           IS:                                                   *   FILE 103
//*                                                                 *   FILE 103
//*               NAME                                              *   FILE 103
//*               STATION (FIRST FOUR BYTES OF INSTALLATION         *   FILE 103
//*                        DATA)                                    *   FILE 103
//*               ACCOUNT                                           *   FILE 103
//*               LOGON PROCEDURE                                   *   FILE 103
//*               INITIAL COMMAND                                   *   FILE 103
//*                                                                 *   FILE 103
//*           ALL OF THE ABOVE ARE THE  STANDARD  RACF  DATA        *   FILE 103
//*           BASE  FIELDS TSO/E  USES  AFTER  THE  CONVERSION      *   FILE 103
//*           FROM SYS1.UADS TO RACF.                               *   FILE 103
//*                                                                 *   FILE 103
//*           FIELDS WHICH REQUIRE RACF AUTHORIZATION TO USE        *   FILE 103
//*           SPECIFIC VALUES WILL BE CHECKED AND ERROR             *   FILE 103
//*           MESSAGES ISSUED IF THE USER IS NOT AUTHORIZED.        *   FILE 103
//*                                                                 *   FILE 103
//*    CONTENTS OF EACH MEMBER OF THIS DATASET                      *   FILE 103
//*                                                                 *   FILE 103
//*   MEMBER   CONTENTS                                             *   FILE 103
//*   ------   --------                                             *   FILE 103
//*   $$ISPF   DOCUMENTATION FOR ISPF SUPPORT FOR THE               *   FILE 103
//*            QUEUE COMMAND                                        *   FILE 103
//*   $$SCRIPT SCRIPT SOURCE FOR THIS DOCUMENT                      *   FILE 103
//*   $DOC     SHORT DESCRIPTION OF MODS                            *   FILE 103
//*   $INSTALL INSTALLATION INSTRUCTIONS (THIS                      *   FILE 103
//*            DOCUMENT)                                            *   FILE 103
//*   $LEVEL   MODIFICATIONS AND SOURCE SYSTEM LEVEL                *   FILE 103
//*   #COPYSCR TUTORIAL PANEL FOR COPYSCRN EDIT MACRO               *   FILE 103
//*   #ELIST   TUTORIAL PANEL FOR ELIST EDIT MACRO                  *   FILE 103
//*   #INFO    TUTORIAL PANEL FOR INFO EDIT MACRO                   *   FILE 103
//*   #SPELL   TUTORIAL PANEL FOR SPELL EDIT MACRO                  *   FILE 103
//*   CDF      SOURCE FOR MVS CONSOLE DIALOG (ASSEMBLER)            *   FILE 103
//*   CDFDATAB PANEL USED BY MVS CONSOLE DIALOG                     *   FILE 103
//*   CDFHELP  TUTORIAL PANEL FOR MVS CONSOLE DIALOG                *   FILE 103
//*   COPYSCRN EDIT MACRO FOR SCREEN COPY                           *   FILE 103
//*   COPYSCT1 TUTORIAL PANEL FOR SCREEN COPY EDIT MACRO            *   FILE 103
//*   COPYSCT2 TUTORIAL PANEL FOR SCREEN COPY EDIT MACRO            *   FILE 103
//*   COPYSC01 PANEL FOR SCREEN COPY EDIT MACRO                     *   FILE 103
//*   DISPLAY  SOURCE CODE FOR QUEUE COMMAND MODULE                 *   FILE 103
//*            DISPLAY MODIFIED FOR ISPF                            *   FILE 103
//*   ELIST    EDIT MACRO FOR LISTING DATA                          *   FILE 103
//*   INFO     EDIT MACRO FOR DISPLAYING DATASET INFORMATION        *   FILE 103
//*   INIT     SOURCE CODE FOR QUEUE COMMAND MODULE                 *   FILE 103
//*            INIT MODIFIED FOR ISPF                               *   FILE 103
//*   QCOMMON  SOURCE CODE FOR QUEUE COMMAND MODULE                 *   FILE 103
//*            QCOMMON MODIFIED FOR ISPF                            *   FILE 103
//*   QUECMDS  ISPF COMMAND TABLE FOR RUNNING QUEUE                 *   FILE 103
//*   QUEPROF  ISPF APPLICATION PROFILE FOR RUNNING QUEUE           *   FILE 103
//*   QUEUE    SOURCE CODE FOR QUEUE COMMAND MODULE                 *   FILE 103
//*            QUEUE MODIFIED FOR ISPF                              *   FILE 103
//*   RACFTSO5 JOBSTREAM (JCL + SOURCE) TO MIGRATE                  *   FILE 103
//*            "FIRST TSO COMMAND" FROM                             *   FILE 103
//*            UADS TO RACF AFTER RUNNING RACONVRT                  *   FILE 103
//*   REPOS    SOURCE CODE FOR QUEUE COMMAND MODULE                 *   FILE 103
//*            REPOS MODIFIED FOR ISPF                              *   FILE 103
//*   SPELL    EDIT MACRO TO CHECK SPELLING                         *   FILE 103
//*   TECMODS  PANEL USED TO INVOKE SOME OF THE MODS.               *   FILE 103
//*   TECZ00   MESSAGES USED BY SEVERAL DIALOGS                     *   FILE 103
//*   TVENQ1   TUTORIAL PANEL FOR GRS/ENQ DIALOG                    *   FILE 103
//*   TVENQ11  TUTORIAL PANEL FOR GRS/ENQ DIALOG                    *   FILE 103
//*   TVENQ12  TUTORIAL PANEL FOR GRS/ENQ DIALOG                    *   FILE 103
//*   TVENQ2   TUTORIAL PANEL FOR GRS/ENQ DIALOG                    *   FILE 103
//*   VBROAD   CLIST USED BY BROADCAST MESSAGE DIALOG               *   FILE 103
//*   VBROADE  ISPF EDIT MACRO USED BY BROADCAST MESSAGE DIALOG     *   FILE 103
//*   VBROADI  CLIST USED TO INITIALIZE BROADCAST MESSAGE DIALOG    *   FILE 103
//*   VBROAD0  PANEL USED BY BROADCAST MESSAGE DIALOG               *   FILE 103
//*   VBROAD1  PANEL USED BY BROADCAST MESSAGE DIALOG               *   FILE 103
//*   VBROAD2  PANEL USED BY BROADCAST MESSAGE DIALOG               *   FILE 103
//*   VCMDEDIC CLIST USED BY COMMAND TABLE EDIT DIALOG              *   FILE 103
//*   VCMDEDIT PANEL USED BY COMMAND TABLE EDIT DIALOG              *   FILE 103
//*   VENQ1    PANEL USED BY GRS/ENQ DIALOG                         *   FILE 103
//*   VENQ2    PANEL USED BY GRS/ENQ DIALOG                         *   FILE 103
//*   VEXIT    PANEL USED WITH FAST EXIT/LOGOFF/LOGON DIALOG        *   FILE 103
//*   VEXITC   CLIST USED WITH FAST EXIT/LOGOFF/LOGON DIALOG        *   FILE 103
//*   VISPFG2  SOURCE + JCL FOR LOGO PROGRAM (PL/I)                 *   FILE 103
//*   VLOGO    PANEL USED WITH LOGO PROGRAM                         *   FILE 103
//*   VLOGOC   CLIST USED WITH LOGO PROGRAM                         *   FILE 103
//*   VLOGON   RACF UPDATE DIALOG SOURCE (BAL)                      *   FILE 103
//*   VLOGONP  PANEL USED BY RACF UPDATE DIALOG                     *   FILE 103
//*   VPC      PANEL USED BY PC FILE TRANSFER DIALOG                *   FILE 103
//*   VPCC     CLIST USED BY PC FILE TRANSFER DIALOG                *   FILE 103
//*   VPCTRAN  CLIST USED BY PC FILE TRANSFER DIALOG                *   FILE 103
//*   VPCT000  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT001  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT002  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT003  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT010  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT011  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT012  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT013  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT014  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT015  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT016  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT017  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VPCT018  TUTORIAL PANEL FOR PC FILE TRANSFER DIALOG           *   FILE 103
//*   VUTL16   SOURCE FOR GRS/ENQ DIALOG (ASSEMBLER)                *   FILE 103
//*                                                                 *   FILE 103
//*                                                                 *   FILE 103
```
