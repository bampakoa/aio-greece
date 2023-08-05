# Ρύθμιση του τοπικού περιβάλλοντος και του χώρου εργασίας

Αυτός ο οδηγός εξηγεί πώς να ρυθμίσετε το περιβάλλον σας για ανάπτυξη Angular χρησιμοποιώντας το [εργαλείο Angular CLI](cli "CLI command reference").
Περιλαμβάνει πληροφορίες σχετικά με τα προαπαιτούμενα, την εγκατάσταση του CLI, τη δημιουργία ενός αρχικού χώρου εργασίας και μιας αρχικής εφαρμογής και την εκτέλεση αυτής της εφαρμογής τοπικά για την επαλήθευση της ρύθμισής σας.

<div class="callout is-helpful">

<header>Δοκιμαστε την Angular χωρις τοπικη ρυθμιση</header>

Εάν είστε νέοι στην Angular, ίσως να θέλετε να ξεκινήσετε με το [Δοκιμάστε το τώρα!](start), το οποίο εξηγεί τα βασικά στοιχεία της Angular στο πλαίσιο μιας έτοιμης βασικής εφαρμογής ηλεκτρονικού καταστήματος που μπορείτε να εξετάσετε και να τροποποιήσετε. Αυτό το αυτόνομο σεμινάριο εκμεταλλεύεται το διαδραστικό περιβάλλον του [StackBlitz](https://stackblitz.com) για ανάπτυξη στο διαδίκτυο. Δεν χρειάζεται να ρυθμίσετε το τοπικό σας περιβάλλον μέχρι να είστε έτοιμοι.

</div>

<a id="devenv"></a>
<a id="prerequisites"></a>

## Προαπαιτούμενα

Για να χρησιμοποιήσετε το Angular framework, θα πρέπει να γνωρίζετε τα εξής:

*   [JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/A_re-introduction_to_JavaScript)
*   [HTML](https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML)
*   [CSS](https://developer.mozilla.org/docs/Learn/CSS/First_steps)

Η γνώση [TypeScript](https://www.typescriptlang.org) είναι χρήσιμη, αλλά δεν απαιτείται.

Για να εγκαταστήσετε την Angular στο τοπικό σας σύστημα, χρειάζεστε τα εξής:

| Απαιτησεις                         | Λεπτομερειες |
|:---                                  |:---     |
| Node.js <a id="nodejs"></a>          | Η Angular απαιτεί μια [ενεργή ή maintenance LTS](https://nodejs.org/about/releases) έκδοση του Node.js.  <div class="alert is-helpful"> Για πληροφορίες σχετικά με συγκεκριμένες απαιτήσεις έκδοσης, ανατρέξτε στην ιδιότητα `engines` στο αρχείο [package.json](https://unpkg.com/browse/@angular/core/package.json). </div> Για περισσότερες πληροφορίες σχετικά με την εγκατάσταση του Node.js, ανατρέξτε στο [nodejs.org](https://nodejs.org "Nodejs.org"). Εάν δεν είστε βέβαιοι ποια έκδοση του Node.js χρησιμοποιείτε στο σύστημά σας, εκτελέστε το `node -v` σε ένα παράθυρο terminal. |
| Διαχειριστής πακέτων npm <a id="npm"></a> | Η Angular, το Angular CLI, και οι εφαρμογές Angular εξαρτώνται από [πακέτα npm](https://docs.npmjs.com/getting-started/what-is-npm) για πολλές δυνατότητες και λειτουργίες. Για λήψη και εγκατάσταση πακέτων npm, χρειάζεστε έναν διαχειριστή πακέτων npm. Αυτός ο οδηγός χρησιμοποιεί το [πρόγραμμα-πελάτη npm](https://docs.npmjs.com/cli/install) της γραμμής εντολών, το οποίο είναι προ-εγκατεστημένο με το `Node.js`. Για να ελέγξετε ότι έχετε εγκαταστήσει το πρόγραμμα-πελάτη npm, εκτελέστε το `npm -v` σε ένα παράθυρο terminal.

<a id="install-the-angular-cli"></a>

## Εγκαταστήστε το Angular CLI

Χρησιμοποιείτε το Angular CLI για να δημιουργείτε projects, να δημιουργείτε κώδικα εφαρμογών και βιβλιοθηκών, και να εκτελείτε μια ποικιλία από συνεχείς εργασίες ανάπτυξης, όπως testing, bundling και deployment.

Για να εγκαταστήσετε το Angular CLI, ανοίξτε ένα παράθυρο terminal και εκτελέστε την ακόλουθη εντολή:

<code-example format="shell" language="shell">

npm install -g &commat;angular/cli<aio-angular-dist-tag class="pln"></aio-angular-dist-tag>

</code-example>

<div class="alert is-helpful">
  <p>Σε υπολογιστές με Windows, η εκτέλεση εντολών PowerShell είναι απενεργοποιημένη από προεπιλογή. Για να επιτρέψετε την εκτέλεση εντολών PowerShell, τα οποία χρειάζονται για την εκτέλεση εντολών npm καθολικά, πρέπει να ορίσετε την εξής <a href="https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies">πολιτική εκτέλεσης</a>:</p>
  <code-example language="sh">
  Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
  </code-example>
  <p>Διαβάστε προσεκτικά το μήνυμα που εμφανίζεται μετά την εκτέλεση της εντολής και ακολουθήστε τις οδηγίες. Βεβαιωθείτε ότι κατανοείτε τις συνέπειες του καθορισμού μιας πολιτικής εκτέλεσης.</p>
</div>

<a id="create-a-workspace-and-initial-application"></a>

## Δημιουργήστε έναν χώρο εργασίας και μια αρχική εφαρμογή

Αναπτύσσετε εφαρμογές στο πλαίσιο ενός [**χώρου εργασίας**](guide/glossary#workspace) Angular.

Για να δημιουργήσετε έναν νέο χώρο εργασίας και μια αρχική εφαρμογή:

1.  Εκτελέστε την εντολή CLI `ng new` και δώστε το όνομα `my-app`, όπως φαίνεται εδώ:

    <code-example format="shell" language="shell">

    ng new my-app

    </code-example>

1.  Η εντολή `ng new` σας ζητά πληροφορίες σχετικά με λειτουργίες που θα συμπεριλάβει στην αρχική εφαρμογή. Αποδεχτείτε τις προεπιλογές πατώντας το πλήκτρο Enter ή Return.

Το Angular CLI εγκαθιστά τα απαραίτητα πακέτα npm της Angular και άλλες εξαρτήσεις. Αυτό μπορεί να διαρκέσει μερικά λεπτά.

Το CLI δημιουργεί έναν νέο χώρο εργασίας και μια απλή εφαρμογή καλωσορίσματος, έτοιμη για εκτέλεση.

<a id="serve"></a>

## Εκτελέστε την εφαρμογή

Το Angular CLI περιλαμβάνει έναν διακομιστή, για να δημιουργήσετε και να τρέξετε την εφαρμογή σας τοπικά.

1.  Πλοηγηθείτε στο φάκελο του χώρου εργασίας, όπως `my-app`.

1.  Εκτελέστε την ακόλουθη εντολή:

    <code-example format="shell" language="shell">

    cd my-app
    ng serve --open

    </code-example>

Η εντολή `ng serve` εκκινεί τον διακομιστή, παρακολουθεί τα αρχεία σας,
και αναδομεί την εφαρμογή καθώς κάνετε αλλαγές σε αυτά τα αρχεία.

Η επιλογή `--open` \(ή για συντομία `-o`\) ανοίγει αυτόματα το πρόγραμμα περιήγησής σας
στο `http://localhost:4200/`.

Εάν η εγκατάσταση και η ρύθμιση ήταν επιτυχείς, θα πρέπει να δείτε μια σελίδα παρόμοια με την παρακάτω.

<div class="lightbox">

<img alt="Καλωσήρθατε στο my-app!" src="generated/images/guide/setup-local/app-works.png">

</div>

## Επόμενα βήματα

*   Για μια πιο εμπεριστατωμένη εισαγωγή στις θεμελιώδεις έννοιες και την ορολογία της αρχιτεκτονικής και σχεδίασης μιας εφαρμογής Angular, διαβάστε την ενότητα [Έννοιες της Angular](guide/architecture).

*   Εργαστείτε μέσω του [σεμιναρίου Tour of Heroes](tutorial/tour-of-heroes), μιας ολοκληρωμένης πρακτικής άσκησης που σας εισάγει στη διαδικασία ανάπτυξης εφαρμογών χρησιμοποιώντας το Angular CLI και περιηγείται σε σημαντικά υποσυστήματα.

*   Για να μάθετε περισσότερα σχετικά με τη χρήση του Angular CLI, ανατρέξτε στην [Επισκόπηση CLI](cli "CLI Overview"). Εκτός από τη δημιουργία του αρχικού χώρου εργασίας και της κατασκευής της εφαρμογής, χρησιμοποιήστε το CLI για να δημιουργήσετε κώδικα Angular όπως components και services. Το CLI υποστηρίζει τον πλήρη κύκλο ανάπτυξης, συμπεριλαμβανομένης της κατασκευής, του testing, του bundling και του deployment.

*   Για περισσότερες πληροφορίες σχετικά με τα αρχεία Angular που δημιουργούνται από το `ng new`, ανατρέξτε στο [Δομή χώρου εργασίας και αρχείων project](guide/file-structure).

<!-- links -->

<!-- external links -->

<!-- end links -->

@reviewed 2022-05-21
