//ListView

import 'package:flutter/material.dart';

void main() {
  List<String> newsChannel = ["JEO NEWS", "EXPRESS NEWS", "SMMA NEWS", "7 NEWS", "JEO SUPPER NEWS", "PTV LIVE", "PTV NEWS"];
  List<String> job = ["Private Channel", "Private Channel", "Private Channel", "Private Channel", "Private Channel", "Private Channel","Govt Channel"];
  List icon = [Icons.account_balance_wallet,   Icons.account_balance_wallet,  Icons.access_alarm_outlined,    Icons.ac_unit,Icons.account_balance_wallet,    Icons.access_alarm_outlined,    Icons.ac_unit   ];
  List trailingicon = [   Icons.account_balance_wallet,   Icons.account_balance_wallet,  Icons.access_alarm_outlined,    Icons.ac_unit,Icons.account_balance_wallet,    Icons.access_alarm_outlined,    Icons.ac_unit];
  List colors = [Colors.green, Colors.red, Colors.blue, Colors.green, Colors.red, Colors.blue, Colors.orangeAccent];
  runApp(
    MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Center(
            child: Text("PAKISTAN NEWS CHENELS"),
          ),
        ),
        body: Material(
          child: Card(
            elevation: 44,
            child: Container(
             margin: EdgeInsets.all(10),
              child: ListView.builder(
                itemCount: newsChannel.length,
                itemBuilder: (context, index) {
                  return Container(
                    color: colors[index],
                    margin: EdgeInsets.all(4),
                    child: ListTile(
                        textColor: Colors.white,
                        iconColor: Colors.white,
                        title: Text(newsChannel[index]),
                        titleAlignment: ListTileTitleAlignment.center,
                        subtitle: Text(job[index]),
                        leading: Icon(icon[index]),
                        trailing: Icon(trailingicon[index])),
                  );
                },
              ),
            ),
          ),
        ),
      ),
    ),
  );
}
