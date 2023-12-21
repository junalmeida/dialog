**Dialog** is a program that will let you present a variety of questions or
display messages using dialog boxes from a shell script.   These  types
of  dialog  boxes  are  implemented  (though  not  all  are necessarily
compiled into dialog):

 >       buildlist, calendar, checklist, dselect, editbox, form, fselect,
 >       gauge, infobox, inputbox, inputmenu, menu, mixedform,
 >       mixedgauge, msgbox (message), passwordbox, passwordform, pause,
 >       prgbox, programbox, progressbox, radiolist, rangebox, tailbox,
 >       tailboxbg, textbox, timebox, treeview, and yesno (yes/no).

You can put more than one dialog box into a script:

o   Use the "--and-widget" token to force **dialog** to proceed to the next
    dialog unless you have pressed ESC to cancel, or

o   Simply  add  the  tokens  for  the next **dialog** box, making a chain.
    Dialog stops chaining  when  the  return  code  from  a  dialog  is
    nonzero, e.g., Cancel or No (see DIAGNOSTICS).

Some  widgets,  e.g.,  checklist,  will  write text to dialog's output.
Normally that is the standard error, but there are options for changing
this:  "--output-fd", "--stderr" and "--stdout".  No text is written if
the Cancel button (or ESC) is pressed; **dialog** exits immediately in that
case.


## Examples
The dialog sources contain several samples of how to use the  different
box  options  and  how  they look.  Just take a look into the directory
samples/ of the source.

## Author
Thomas E. Dickey (updates for 0.9b and beyond)

## Contributors
* Kiran Cherupally - the mixed form and mixed gauge widgets.

* Tobias C. Rittweiler

* Valery Reznic - the form and progressbox widgets.

* Yura Kalinichenko adapted the gauge widget as "pause".

This  is  a  rewrite (except as needed to provide compatibility) of the
earlier version of dialog 0.9a, which lists as authors:

*   Savio Lam - version 0.3, "dialog"

*   Stuart Herbert - patch for version 0.4

*   Marc Ewing - the gauge widget.

*   Pasquale De Marco "Pako" - version 0.9a, "cdialog"