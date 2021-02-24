# project-mobile1
	
	Input-data
	import 'package:flutter/material.dart';
	

	void main() {
	  runApp(MaterialApp(
	    home: Informasi(),
	  ));
	}
	

	class Informasi extends StatelessWidget {
	  Widget build(BuildContext context) {
	    return Scaffold(
	      appBar: AppBar(
	        title: Text('Informasi Mahasiswa'),
	      ),
	      floatingActionButton: FloatingActionButton.extended(
	          icon: Icon(Icons.add),
	          label: Text('Input Data'),
	          onPressed: () {
	          // Navigasi ke rute kedua (Input Data).
	            Navigator.push(
	              context,
	              MaterialPageRoute(builder: (context) => InputData()),
	            );
	          }),
	      body: ListView(
	        children: ListTile.divideTiles(
	          context: context,
	          tiles: [
	            ListTile(
	              leading: Icon(Icons.people),
	              title: Text("rivani margaretta"),
	              subtitle: Text("perempuan"),
	              trailing: Text("Komputer"),
	            ),
	            ListTile(
	              leading: Icon(Icons.people),
	              title: Text("riski "),
	              subtitle: Text("laki-laki"),
	              trailing: Text("Ekonomi"),
	            ),
	          ],
	        ).toList(),
	      ),
	    );
	  }
	}import 'package:flutter/material.dart';
	

	void main() {
	  runApp(MaterialApp(
	    home: Informasi(),
	  ));
	}

	class InputData extends StatelessWidget {
	  Widget build(BuildContext context) {
	    return Scaffold(
	      appBar: AppBar(
	        title: Text("Input Data Mahasiswa"),
	      ),
	      body: Container(
	        padding: EdgeInsets.all(20.0),
	        child: Column(
	          children: [
	            TextField(
	              decoration: InputDecoration(labelText: "Input Nama Mahasiswa"),
	            ),
	            RadioListTile(
	              title: Text('Laki-laki'),
	              value: null,
	              groupValue: null,
	              onChanged: null,
	            ),
	            RadioListTile(
	              title: Text('Perempuan'),
	              value: null,
