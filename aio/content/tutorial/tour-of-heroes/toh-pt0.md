# Δημιουργήστε ένα νέο project

Χρησιμοποιήστε την εντολή `ng new` για να ξεκινήσετε τη δημιουργία της εφαρμογής **Tour of Heroes**.

Αυτό το σεμινάριο:

1.  Ρυθμίζει το περιβάλλον σας.
2.  Δημιουργεί έναν νέο χώρο εργασίας και ένα αρχικό project της εφαρμογής.
3.  Εκτελεί την εφαρμογή.
4.  Κάνει αλλαγές στην εφαρμογή.

<div class="alert is-helpful">

Για να δείτε τον κώδικα της εφαρμογής, ανατρέξτε στο <live-example></live-example>.

</div>

## Ρυθμίστε το περιβάλλον σας

Για να ρυθμίσετε το περιβάλλον ανάπτυξής σας, ακολουθήστε τις οδηγίες στο [Ρύθμιση τοπικού περιβάλλοντος](guide/setup-local "Ρύθμιση για τοπική ανάπτυξη").

## Δημιουργήστε έναν νέο χώρο εργασίας και μια αρχική εφαρμογή

Αναπτύσσετε εφαρμογές στο πλαίσιο ενός [χώρου εργασίας](guide/glossary#workspace) Angular.
Ένας *χώρος εργασίας* περιέχει τα αρχεία για ένα ή περισσότερα [projects](guide/glossary#project).
Ένα *project* είναι το σύνολο των αρχείων που περιλαμβάνει μια εφαρμογή ή μια βιβλιοθήκη.

Για να δημιουργήσετε έναν νέο χώρο εργασίας και ένα αρχικό project:

  1.  Βεβαιωθείτε ότι δεν βρίσκεστε ήδη σε φάκελο χώρου εργασίας Angular.
      Για παράδειγμα, εάν είστε ήδη στον χώρο εργασίας "Πώς να ξεκινήσετε" από προηγούμενη άσκηση, μεταφερθείτε ένα επίπεδο πάνω.
  
  2.  Εκτελέστε την εντολή `ng new` ακολουθούμενη από το όνομα της εφαρμογής όπως φαίνεται εδώ:

      <code-example format="shell" language="shell">

      ng new angular-tour-of-heroes

      </code-example>

  3.  Η εντολή `ng new` σάς ζητά πληροφορίες σχετικά με τις λειτουργίες που θα συμπεριλάβει στο αρχικό project. Αποδεχτείτε τις προεπιλογές πατώντας το πλήκτρο Enter ή Return.

Η εντολή `ng new` εγκαθιστά τα απαραίτητα πακέτα `npm` και άλλες εξαρτήσεις που απαιτεί η Angular. Αυτό μπορεί να διαρκέσει μερικά λεπτά.

Η εντολή `ng new` δημιουργεί επίσης τον ακόλουθο χώρο εργασίας και τα αρχεία του αρχικού project:

*   Έναν νέο χώρο εργασίας, με έναν κύριο φάκελο που ονομάζεται `angular-tour-of-heroes`
*   Ένα αρχικό project της βασικής εφαρμογής στον υποφάκελο `src/app`
*   Σχετικά αρχεία παραμετροποίησης

Το αρχικό project της εφαρμογής περιέχει μια απλή εφαρμογή, έτοιμη για εκτέλεση.

## Εκτελέστε την εφαρμογή

Μεταβείτε στον φάκελο του χώρου εργασίας και ξεκινήστε την εφαρμογή.

<code-example format="shell" language="shell">

cd angular-tour-of-heroes
ng serve --open

</code-example>

<div class="alert is-helpful">

Η εντολή `ng serve`:

* Δημιουργεί την εφαρμογή
* Ξεκινά τον διακομιστή ανάπτυξης
* Παρακολουθεί τα αρχεία προέλευσης
* Ανανεώνει την εφαρμογή καθώς κάνετε αλλαγές

Η επιλογή `--open` ανοίγει το πρόγραμμα περιήγησης στο `http://localhost:4200`.

</div>

Θα πρέπει να δείτε την εφαρμογή να εκτελείται στο πρόγραμμα περιήγησής σας.

## Angular components

Η σελίδα που βλέπετε είναι το *κέλυφος της εφαρμογής*.
Το κέλυφος ελέγχεται από ένα **component** της Angular που ονομάζεται `AppComponent`.

Τα *Components* είναι τα θεμελιώδη δομικά στοιχεία των εφαρμογών Angular.
Εμφανίζουν δεδομένα στην οθόνη, παρακολουθούν την εισαγωγή δεδομένων από τον χρήστη και ενεργούν με βάση αυτά τα δεδομένα.

## Κάντε αλλαγές στην εφαρμογή

Ανοίξτε το project στο αγαπημένο σας πρόγραμμα επεξεργασίας ή IDE. Μεταβείτε στον φάκελο `src/app` για να επεξεργαστείτε την αρχική εφαρμογή.

Στο IDE, εντοπίστε τα αρχεία, που αποτελούν το `AppComponent` που μόλις δημιουργήσατε:

| Αρχεια                | Λεπτομερειες |
|:---                  |:---     |
| `app.component.ts`   | ο κώδικας του class του component, γραμμένος σε TypeScript. |
| `app.component.html` | Το template του component, γραμμένο σε HTML.                |
| `app.component.css`  | Τα στυλ CSS του component.                                  |

<div class="alert is-important">

Όταν εκτελέσατε το `ng new`, η Angular δημιούργησε προδιαγραφές για τα test για τη νέα σας εφαρμογή.
Ωστόσο, η πραγματοποίηση αυτών των αλλαγών παραβιάζει τις νέες προδιαγραφές σας.

Αυτό δεν θα είναι πρόβλημα, επειδή το Angular testing είναι εκτός θέματος από αυτό το σεμινάριο και δεν θα χρησιμοποιηθεί.

Για να μάθετε περισσότερα σχετικά με το Angular testing, ανατρέξτε στο [Testing](guide/testing).

</div>

### Αλλάξτε τον τίτλο της εφαρμογής

Ανοίξτε το `app.component.ts` και αλλάξτε την τιμή της ιδιότητας `title` σε 'Tour of Heroes'.

<code-example header="app.component.ts (Ιδιότητα title του class)" path="toh-pt0/src/app/app.component.ts" region="set-title"></code-example>

Ανοίξτε το `app.component.html` και
διαγράψτε το προεπιλεγμένο template που δημιουργήθηκε από το `ng new`.
Αντικαταστήστε το με την ακόλουθη γραμμή HTML.

<code-example header="app.component.html (template)" path="toh-pt0/src/app/app.component.html"></code-example>

Οι διπλές αγκύλες είναι η σύνταξη *interpolation binding* της Angular.
Αυτό το interpolation binding παρουσιάζει την τιμή της ιδιότητας `title` του component
μέσα στο στοιχείο header του HTML.

Το πρόγραμμα περιήγησης ανανεώνει την εφαρμογή και εμφανίζει τον νέο τίτλο.

<a id="app-wide-styles"></a>

### Προσθέστε στυλ στην εφαρμογή

Οι περισσότερες εφαρμογές προσπαθούν να έχουν μια συνεπή εμφάνιση σε όλη την εφαρμογή.
Η εντολή `ng new` δημιούργησε ένα κενό `styles.css` για αυτόν τον σκοπό.
Τοποθετήστε εκεί τα στυλ της εφαρμογής σας.

Ανοίξτε το `src/styles.css` και προσθέστε τον παρακάτω κώδικα στο αρχείο.

<code-example header="src/styles.css (απόσπασμα)" path="toh-pt0/src/styles.1.css"></code-example>

## Επισκόπηση τελικού κώδικα

Εδώ είναι τα αρχεία κώδικα που συζητήθηκαν σε αυτήν τη σελίδα.

<code-tabs>
    <code-pane header="src/app/app.component.ts" path="toh-pt0/src/app/app.component.ts"></code-pane>
    <code-pane header="src/app/app.component.html" path="toh-pt0/src/app/app.component.html"></code-pane>
    <code-pane header="src/styles.css (απόσπασμα)" path="toh-pt0/src/styles.1.css"></code-pane>
</code-tabs>

## Περίληψη

*   Δημιουργήσατε την αρχική δομή της εφαρμογής χρησιμοποιώντας την εντολή `ng new`
*   Μάθατε ότι τα components της Angular εμφανίζουν δεδομένα
*   Χρησιμοποιήσατε τις διπλές αγκύλες του interpolation για να εμφανίσετε τον τίτλο της εφαρμογής

@reviewed 2022-11-06
