---
title: Send a program, not a data structure
---

Alan Kay on ever expanding requirements

<https://www.quora.com/Should-web-browsers-have-stuck-to-being-document-viewers>

> Footnote about “Ever expanding requirements at Parc” (prompted by Phillip Remaker’s comment and question)
> 
> When Gary Starkweather invented and got the first laser printer going very quickly, and at astounding speeds (a page per second, 500 pixels per inch), there was a push to get one of these on the networked Altos (for which the Ethernet had been invented). The idea was to use an Alto as a server that could set up and run a laser printer to rapidly print high quality documents.
> 
> Several of the best graphics people at Parc created an excellent “printing standard” for how a document was to be sent to the printer. This data structure was parsed at the printer side and followed to set up printing.
> 
> But just a few weeks after this, more document requirements surfaced and with them additional printing requirements.
> 
> This led to a “sad realization” that **sending a data structure to a server is a terrible idea if the degrees of freedom needed on the sending side are large**.
> 
> And eventually, this led to a “happy realization”, that sending a program to a server is a very good idea if the degrees of freedom needed on the sending side are large.
> 
> John Warnock and Martin Newell were experimenting with a simple flexible language that could express arbitrary resolution independent images — called “JAM” (for “John And Martin” — and it was realized that sending JAM programs to the printer was a much better idea than sending a data structure.
> 
> This is because a universal interpreter can both be quite small and also can have more degrees of freedom than any data structure (that is not a program). The program has to be run in a protected address space in the printer computer, but it can be granted access to a bit-buffer, and whatever it does to it can then be printed out “blindly”.
> 
> This provides a much better match up between a desktop publishing system (which will want to print on any of the printers available, and shouldn’t have to know about their resolutions and other properties), and a printer (which shouldn’t have to know anything about the app that made the document).
> 
> “JAM” eventually became Postscript (but that’s another story).
> 
> Key Point: **“sending a program, not a data structure” is a very big idea (and also scales really well if some thought is put into just how the program is set up).**