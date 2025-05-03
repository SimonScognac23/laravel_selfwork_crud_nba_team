Italiano:

Nel mio controller ArticleController, ho implementato diverse funzioni per gestire le operazioni CRUD (Create, Read, Update, Delete) per gli articoli.

index(): In questo metodo recupero tutti gli articoli dal database usando il modello Article e il metodo all(). Dopodiché, passo i dati alla vista article.index per visualizzarli.

create(): In questo metodo restituisco la vista del form per creare un nuovo articolo, senza alcuna logica aggiuntiva, poiché il form è gestito direttamente dalla vista.

store(): Qui gestisco la creazione di un nuovo articolo. Prima controllo se l'utente ha caricato un'immagine. Se l'immagine è presente, la salvo nella cartella public/img. In caso contrario, assegno un'immagine predefinita. Dopo di che, creo un nuovo articolo nel database con i dati forniti. Infine, ritorno alla stessa pagina con un messaggio di successo.

show(): Questo metodo è progettato per visualizzare i dettagli di un articolo specifico, che viene passato alla vista article.show tramite il metodo compact.

edit(): Qui recupero un articolo specifico utilizzando il suo id e lo passo alla vista di modifica per consentire all'utente di aggiornarlo.

update(): In questo metodo, aggiorno un articolo esistente. Dopo aver convalidato i dati inviati dal form, aggiorno l'articolo nel database con i nuovi valori. Se l'aggiornamento ha successo, reindirizzo l'utente con un messaggio di successo.

destroy(): Infine, nel metodo destroy(), elimino un articolo dal database e reindirizzo l'utente alla pagina di elenco articoli con un messaggio di conferma.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
English:

In my ArticleController, I implemented several methods to handle the CRUD (Create, Read, Update, Delete) operations for articles.

index(): In this method, I retrieve all articles from the database using the Article model and the all() method. Then, I pass the data to the article.index view to display them.

create(): In this method, I return the view for the form to create a new article. There is no additional logic here, as the form is handled directly in the view.

store(): Here, I handle the creation of a new article. First, I check if the user has uploaded an image. If the image is present, I save it to the public/img folder. If not, I assign a default image. Then, I create a new article in the database with the provided data. Finally, I return to the same page with a success message.

show(): This method is designed to display the details of a specific article, which is passed to the article.show view using the compact method.

edit(): Here, I retrieve a specific article using its id and pass it to the edit view, allowing the user to update it.

update(): In this method, I update an existing article. After validating the data sent from the form, I update the article in the database with the new values. If the update is successful, I redirect the user with a success message.

destroy(): Finally, in the destroy() method, I delete an article from the database and redirect the user to the articles listing page with a confirmation message.
