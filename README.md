# ativ_widget

import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Column(children: [
      Row(children: [
        
        meuContainer ('Nome: \n Cargo: \n Tel: \n Email:', Colors.blue, 150, 150),
        meuContainer ('Nome: \n Cargo: \n Tel: \n Email:', Colors.blue, 150, 150),
        meuContainer ('Nome: \n Cargo: \n Tel: \n Email:', Colors.blue, 150, 150),
      ]),
      Row(children: [
        meuContainer ('Nome: \n Cargo: \n Tel: \n Email:', Colors.blue, 150, 150),
        meuContainer ('Nome: \n Cargo: \n Tel: \n Email:', Colors.blue, 150, 150),
        meuContainer ('Nome: \n Cargo: \n Tel: \n Email:', Colors.blue, 150, 150),
      ])

    ]);
  }
}


meuContainer (String nome, Color cor, double largura, double altura){
  
  return Container(
          margin: const EdgeInsets.all(10.0),
          color: Colors.blue,
          width: largura,
          height: altura,
          child:  Column (children: [
           Row (children: [
             Text (nome),
            Image.network ('https://m.media-amazon.com/images/I/81k78iqhzoL._AC_SL1500_.jpg',
                        width: 100,
          height: 100,  )
           ] ) ] )
  );
          
 }
