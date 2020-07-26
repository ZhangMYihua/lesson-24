.doc .collection is how you query firestore db and get back an object
.doc used for crud and gets document snapShot object
.collection get query snapShot obejct
.get pulls out snapShot object to detrmine with our code wether or not there is a reference

query refObject and query snapShot is what you get from fire store

ref object that represents current place in database
  get by calling firestore.doc('/users/:userId')
  or firestore.collections('/users')
  does not have actual data of the collections, but properties that tell us details(id or path etc) about it
  or the Snapshot object which gives us the data we are looking for

to retreive the snapShot call .get()