# CBT452
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 452 is from Dan Dalby and contains a collection of his    *   FILE 452
//*           programs and utilities, which he has been distribu-   *   FILE 452
//*           ting over the Internet.  Dan retains ownership of     *   FILE 452
//*           the programs, but has given permission for them to    *   FILE 452
//*           be distributed on the CBT Tape.  Please see the       *   FILE 452
//*           general disclaimer information on File 001 of the     *   FILE 452
//*           CBT Tape, and what it says regarding "owned files".   *   FILE 452
//*                                                                 *   FILE 452
//*    Licensed material-program, Property of zOS.JES2@Gmail.com    *   FILE 452
//*    All Rights Reserved by zOS.JES2@Gmail.com                    *   FILE 452
//*                                                                 *   FILE 452
//*    As with the CBT source rules, this code may be freely        *   FILE 452
//*    distributed.  However I retain ownership of this code.       *   FILE 452
//*    Thus it may not be used, fully or in part, in a              *   FILE 452
//*    commercial product or sold in any way.                       *   FILE 452
//*                                                                 *   FILE 452
//*    Description of the programs included here:                   *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     Add to existing allocations (ADDTO)                         *   FILE 452
//*     Updated July 1, 1999                                        *   FILE 452
//*                                                                 *   FILE 452
//*     Many users want their own personal libraries to be          *   FILE 452
//*     allocated in front of the libraries that are allocated      *   FILE 452
//*     within the LOGON procedure. Normally, this means that       *   FILE 452
//*     the user has to re-allocate the DD, specifying all of       *   FILE 452
//*     the libraries with their own as the first library. If       *   FILE 452
//*     the libraries that are in the LOGON procedure get           *   FILE 452
//*     renamed or deleted due to maintenance, the user's           *   FILE 452
//*     allocation fails, leaving them without that specific DD     *   FILE 452
//*     allocated at ALL.  With this command, you simply let        *   FILE 452
//*     the LOGON procedure do it's thing, and in your initial      *   FILE 452
//*     logon CLIST/REXX specify the libraries you want in          *   FILE 452
//*     front. The re-allocation occurs, without the user           *   FILE 452
//*     needing to know all the LOGON procedure's library           *   FILE 452
//*     names.                                                      *   FILE 452
//*                                                                 *   FILE 452
//*     Note: ADDTO can NOT extend DDs that are OPEN. In other      *   FILE 452
//*     words, ISPxLIB's can't be ADDTO'd once you are in ISPF.     *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     Fast Catalog List Command (CATL)                            *   FILE 452
//*     Updated July 2, 1999                                        *   FILE 452
//*                                                                 *   FILE 452
//*     The TSO LISTCAT command seems to gather every smidgen       *   FILE 452
//*     of information necessary about a dataset, even if it is     *   FILE 452
//*     not going to display it on your screen. This command        *   FILE 452
//*     only gets the required information, making it quite a       *   FILE 452
//*     bit faster. There are additional keywords to change how     *   FILE 452
//*     CATL displays the output. Try the "SIDEWAYS" keyword on     *   FILE 452
//*     a GDG base.                                                 *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     List Dataset Information (LDS)                              *   FILE 452
//*                                                                 *   FILE 452
//*     This command lets you list information about your           *   FILE 452
//*     libraries that you really can't get easily any other        *   FILE 452
//*     way.  Actually, until TSO/E, some of this information       *   FILE 452
//*     wasn't available at all.                                    *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     DASD Pack Map (PACKMAP)                                     *   FILE 452
//*     Updated July 2, 1999                                        *   FILE 452
//*                                                                 *   FILE 452
//*     Occasionally, you need to know the physical layout of a     *   FILE 452
//*     volume. This utility generates a MAP for you. The           *   FILE 452
//*     output report gives you the relative track, extent          *   FILE 452
//*     length, extent number, CCHH and DCB information for         *   FILE 452
//*     every dataset on the volume. The freespace extents and      *   FILE 452
//*     VTOC information are also displayed in this report.         *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     PDS Rescue (PRU)                                            *   FILE 452
//*     Updated August 11, 2004                                     *   FILE 452
//*                                                                 *   FILE 452
//*     Have you ever hit SAVE in ISPF when you meant to enter      *   FILE 452
//*     CANCEL? I have. This utility allows you to get the          *   FILE 452
//*     original member back. The original library is left          *   FILE 452
//*     untouched, and a new library is created with all the        *   FILE 452
//*     OLD members.  Unfortunately, this does not work on PDSE     *   FILE 452
//*     libraries, or after a PDS has been compressed.              *   FILE 452
//*                                                                 *   FILE 452
//*     A REXX exec has been provided by one of the users of        *   FILE 452
//*     this utility. This makes it easier than ever to recover     *   FILE 452
//*     member(s).                                                  *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     Return/Abend Code Generator (RETCODE)                       *   FILE 452
//*     Updated July 14, 1999                                       *   FILE 452
//*                                                                 *   FILE 452
//*     Need to test the "COND=" or "IF" logic of your batch        *   FILE 452
//*     jobs?  This tool lets you generate a step with any          *   FILE 452
//*     return code or User/System ABEND code.                      *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     Dynamic Steplib (STEPLIB)                                   *   FILE 452
//*     Updated ...ongoing...                                       *   FILE 452
//*                                                                 *   FILE 452
//*     With the deficiencies of ISPLLIB, and the other             *   FILE 452
//*     "tasklib" capabilities provided by IBM, sometimes you       *   FILE 452
//*     really need a STEPLIB. I've found it easier to simply       *   FILE 452
//*     forget the other facilities, and use STEPLIB                *   FILE 452
//*     exclusively. This tool allows you to create, alter or       *   FILE 452
//*     remove your STEPLIB at any time during the life of your     *   FILE 452
//*     TSO session.                                                *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     User/System Symbols (USERINFO)                              *   FILE 452
//*     Updated April 2, 2000                                       *   FILE 452
//*                                                                 *   FILE 452
//*     Ever need to know your TSO terminal ID, the JES             *   FILE 452
//*     subsystem you're running under or a raft of other system    *   FILE 452
//*     or user related items within a CLIST or REXX? Of course,    *   FILE 452
//*     in a REXX EXEC, you can bounce through control blocks,      *   FILE 452
//*     but wouldn't it be easier to have it available in a         *   FILE 452
//*     defined symbol. Actually, this tool was created way         *   FILE 452
//*     back, before REXX was available, and CLIST was the way      *   FILE 452
//*     to go. With USERINFO, the system and user information is    *   FILE 452
//*     readily available in a &SYSxxxx variable. Simply invoke     *   FILE 452
//*     the USERINFO program at the beginning of the CLIST, and     *   FILE 452
//*     all these symbols magically appear. Recently, a user        *   FILE 452
//*     needed to know what day of the week it was, so &SYSWDAY     *   FILE 452
//*     was added.  The system symbols defined in IEASYMxx as       *   FILE 452
//*     well as the current RACF USER and GROUP names are now       *   FILE 452
//*     available.                                                  *   FILE 452
//*                                                                 *   FILE 452
//*     If you'd like additional variables, and know the            *   FILE 452
//*     control block location, simply Email me and I'll add        *   FILE 452
//*     it.                                                         *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     Who's Got my Dataset (WHOSGOT)                              *   FILE 452
//*                                                                 *   FILE 452
//*     When trying to edit or allocate a library, occasionally     *   FILE 452
//*     you will get a "dataset in use" message.  This tool         *   FILE 452
//*     lets you ask the question... "WHO'S GOT MY FILE"?           *   FILE 452
//*                                                                 *   FILE 452
//*       ----------------------------------------------------      *   FILE 452
//*                                                                 *   FILE 452
//*     IEFUJV System Exit Routine.                                 *   FILE 452
//*                                                                 *   FILE 452
//*     This routine will translate a variety of variables on       *   FILE 452
//*     JCL SET statements.  This allows the use of date and        *   FILE 452
//*     system symbols within batch JCL.                            *   FILE 452
//*                                                                 *   FILE 452
```
