﻿#Twitter Visualisation
Κασταμπολίδου Καλλιόπη - Π2012016, 
Παπαγιαννίδης Ιωάννης - Π2012067
##Τελική αναφορά
(ο κώδικας της εργασίας βρίσκεται εδώ: https://github.com/p12papa1/What-Good-You-Read)
<font="22"><p align="center"><b>What Good You Read?</font></b><br>http://whatgoodyouread.herokuapp.com/</br></p>

<p align="center"><b>Σύνοψη</b></p>
Η παρούσα εργασία αποτελεί μια χαρτογράφηση της κοινότητας του twitter, σχετικά με το τι διαβάζουν οι χρήστες αυτήν την εποχή. Σε ένα περιβάλλον που προσπαθεί να προσομοιώσει, κατά μία έννοια, μια βιβλιοθήκης, ο χρήστης που επισκέπτεται τη σελίδα μας μπορεί να εξετάσει τι διαβάζει ο υπόλοιπος κόσμος αυτή τη στιγμή. Μπορεί να πάρει ιδέες για το επόμενο βιβλίο του, αφού το twitter, μεταξύ άλλων, θεωρείται εξαιρετική πηγή για βιβλιοπροτάσεις.
<p align="center"><b>Εισαγωγή</b></p>
Σκοπός της εργασίας αυτής είναι να οπτικοποιήσουμε/παρατηρήσουμε τι βιβλία διαβάζει η κοινότητα του twitter. Οι χρήστες του twitter τείνουν να ενημερώνουν τους διαδικτυακούς τους "ακόλουθους" για την καθημερινότητά τους και τις συνήθειες τους. Ένα από τα πράγματα που συνηθίζουν κάποιοι να "τουιτάρουν" είναι και το βιβλίο που διαβάζουν αυτή την περίοδο. Ο ρόλος, λοιπόν, αυτής της εργασίας είναι να συγκεντρώσει τα βιβλία που διαβάζουν οι χρήστες του twitter, με σκοπό και άλλοι αναγνώστες να παίρνουν ιδέες για το επόμενο βιβλίο τους, αλλά και να χαρτογραφήσουμε κατά μία έννοια τις προτιμήσεις των χρηστών στα βιβλία. 
<p align="center"><b>Επιλογή Εργαλείων</b></p>
Η οπτικοποίηση των δεδομένων έγινε εξ'ολοκλήρου στο περιβάλλον της P5.js, η οποία είναι μια βιβλιοθήκη της javascript εμπνευσμένη από το Processing, για γραφικά σε browsers (φυλλομετρητές). Για το διαδικτυακό κομμάτι της εφαρμογής χρησιμοποιήσαμε node.js και ορισμένα modules του framework αυτού. Αυτά ήταν το Express, για να απαντάει σε http requests και το Twit, με το οποίο ανακτούμε τα δεδομένα μας (tweets) μέσω του Twitter REST API. Τέλος, χρησιμοποιήσαμε την πλατφόρμα heroku, η οποία μας έδωσε την δυνατότητα να "τρέξουμε" την εφαρμορή μας στο διαδίκτυο.

<p align="center"><b>Διαδικασία Ανάπτυξης</b></p> 
Αρχικά, αποφασίστηκε ότι η φράση που θα αναζητούμε είναι "currentlyreading", είτε σαν hashtag(#), είτε σαν φράση μέσα στο κείμενο-tweet. Στην πορεία, αναζητήσαμε το κατάλληλο φόντο για την εφαρμογή μας και καταλήξαμε σε μια απεικόνισης βιβλιοθήκης. Η οπτικοποίηση των μηνυμάτων γίνεται με την βοήθεια της P5.js, σαν βιβλία που μοιάζουν να πέφτουν από τα ράφια της βιβλιοθήκης. Κάθε βιβλίο περιέχει και ένα tweet από αυτά που τραβάμε με την βοήθεια των Express και Twit της node.js. Οι απεικονίσεις των βιβλίων δημιουργήθηκαν στο photoshop. Ουσιαστικά, πρόκειται για ένα βιβλίο σε 6 διαφορετικά χρώματα (μπλε, χρυσό, γκρι, κίτρινο, πράσινο και κόκκινο). Όλες οι αποχρώσεις που επιλέχθηκαν ταιριάζουν χρωματικά και με το φόντο της εφαρμογής. Για την εμφάνιση του μηνύματος χρησιμοποιήσαμε το λευκό χρώμα, για να κάνει αντίθεση με τα υπόλοιπα στοιχεία, με μέγεθος γραμματοσειράς 16, bold helvetica. Με κάθε καινούριο βιβλίο που εμφανίζεται, εμφανίζεται και ένα διαφορετικό tweet. Για να μπορέσουμε να έχουμε πρόσβαση στο API του twitter χρειάστηκε να δηλώσουμε την εφαρμογή μας στη σελίδα του twitter, για να αποκτήσουμε τα απαραίτητα credentials.
Με την P5.js δημιουργήσαμε την οπτικοποίηση των δεδομένων. Η P5.js είναι αρκετά παρόμοια με την γλώσσα Processing, μόνο που χρησιμοποιεί σαν βάση την Javascript αντί για την Java. Αρχικά φορτώνουμε τις εικόνες που θα χρειαστούμε (background και 6 εικόνες από βιβλία σε διαφορετικά χρώματα) και ένα json αρχείο που περιέχει τα tweets. Στην συνέχεια, δημιουργούμε αντικείμενα για κάθε tweet και τα "συνδέουμε" με μια εικόνα βιβλίου. Τέλος, δημιουργείται το animation της ρήψης των βιβλίων και η σελίδα περιμένει την διάδραση του χρήστη για να εμφανίσει καινούργια tweets. Το Node.js είναι ένα framework το οποίο επιτρέπει την javascript να τρέχει στη μεριά του server και βοηθάει με αυτό τον τρόπο την ανάπτυξη web ερφαρμογών. Το Node.js στηρίζεται στα modules, τα οποία είναι κομμάτια κώδικα για συγκεκριμένες εργασίες τα οποία προσφέρονται έτοιμα από τον package manager του. Εμείς συγκεκριμένα χρησιμοποιήσαμε το Express module το οποίο απαντάει σε http requrests και "σερβίρει" αρχεία όπως html ή JSON. Επίσης, το Twit module επικοινωνεί με το Twitter και στέλνει ερωτήματα REST για το ποια tweets περιέχουν τη φράση "currentlyreading" και στην συνέχεια γυρνάει ένα JSON αρχείο το οποίο
αντιγράφουμε σε ένα καινούργιο JSON αρχείο για να το φορτώσει η P5.js. Τέλος, το heroku είναι μια cloud πλατφόρμα που επιτρέπει να κάνουμε διαθέσιμη στο διαδίκτυο την εφαρμογή μας απλά φορτώνοντας τον κώδικα στους server του.
<p align="center"><b>Διάγραμμα Λειτουργίας Συστήματος</b></p> 
Με το που φορτώσει η ιστοσελίδα μας εμφανίζεται η εικόνα μιας βιβλιοθήκης ως κύριο φόντο και ξεκινούν τα βιβλία να "πέφτουν" από την κορυφή. Μόλις σταματήσουν ο χρήστης μπορεί να τοποθετήσει τον κέρσορά του επάνω τους για να δει το tweet. Τα βιβλία είναι κινούμενες 
εικόνες σε 6 διαφορετικά χρώματα, τα οποία σταματάνε λίγο πριν το τέλος του φόντου. Τα χρώματα επιλέγονται τυχαία κάθε φορά, γι'αυτό είναι πιθανό να τύχουν περισσότερα από δύο με το ίδιο χρώμα. Μόλις τα βιβλία σταματήσουν να πέφτουν, τότε και μόνο τότε μπορεί ο χρήστης να δει το tweet. Σε κάθε βιβλίο κρύβεται από ένα tweet. Είναι πιθανό κάποια βιβλία να έχουν το ίδιο μήνυμα, αλλά πρόκειται για re-tweet του αρχικού. Μόλις ο χρήστης διαβάσει ένα μήνυμα, μπορεί να κάνει κλικ επάνω στο βιβλίο που διάβασε και αμέσως θα ξεκινήσει να πέφτει ένα καινούριο βιβλίο με ένα διαφορετικό μήνυμα. Ανάλογα με το μέγεθος της κάθε οθόνης, ο αριθμός των βιβλίων προσαρμόζεται στις διαστάσεις του παραθύρου. Την πρώτη φορά που θα βρεθεί κάποιος στη σελίδα μας θα ξεκινήσουν να πέφτουν αυτόματα βιβλία με τα πρώτα tweets και από εκεί και πέρα είναι στην ευχέρεια του χρήστη ποια βιβλία θα κρατήσει και ποια θα διώξει. Το heroku app είναι μια δωρεάν πλατφόρμα, η οποία φιλοξενεί πολλά projects. Για τον λόγο αυτό, η πρώτη επίσκεψη στη σελίδα μας αργεί, ωστόσο με κάθε επίσκεψη ο χρόνος του loading μειώνεται.
<p align="center"><b>Ενδεικτικές Εικόνες</b></p> 
Την πρώτη φορά που φορτώνει η σελίδα:
![Alt text](13324283_10205554644895650_1575385906_o.png?raw=true "1")
ξεκινούν να πέφτουν τα βιβλία και μόλις φτάσουν στο τέλος σταματάνε.
![Alt text](13288549_10205554644935651_857141513_o.png?raw=true "2")
![Alt text](13334700_10205554645055654_754576839_o.png?raw=true "3")
Η εμφάνιση του μηνύματος γίνεται αφού τοποθετήσει ο χρήστης το ποντίκι του πάνω σε κάποιο βιβλίο.
![Alt text](13313697_10205554644455639_1935195532_o.png?raw=true "4")
Με ένα κλικ επάνω στο βιβλίο, ξεκινά να πέφτει ένα νέο. 
![Alt text](13313628_10205554644975652_1331475980_o.png?raw=true "5")
<p align="center"><b>Συμπεράσματα</b></p> 
Όπως αναφέρει και το άρθρο[1], το twitter αποτελεί μια από τις καλύτερες πηγές για να προτείνει σε κάποιον βιβλία. Με την δική μας εργασία, αυτό γίνεται λίγο πιο εύκολο, αφού αυτόματα συγκεντρώνουμε τους τίτλους που ενδιαφέρουν τους χρήστες αυτήν την περίοδο. Εάν κάποιος ενδιαφέρεται να δει τι διαβάζει η κοινότητα του twitter ή ψάχνει ιδέες για το επόμενο βιβλίο που θα διαβάσει, η εργασία μας είναι ακριβώς αυτό που χρειάζεται.
 

[1]http://www.telegraph.co.uk/culture/books/11325722/mark-zuckerberg-book-club-facebook.html




