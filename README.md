📦 Flutter GridView.count Example
📖 Overview

GridView.count is a Flutter widget that creates a scrollable, 2D array of widgets with a fixed number of columns.
It’s the simplest way to build a grid when you know exactly how many columns you want.

✨ Features

Easy to use with a fixed number of columns.

Automatically scrollable if content overflows.

Supports spacing between items (both horizontal and vertical).

Great for displaying uniform items like images, cards, products, or lists.

🧑‍💻 Example Code
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: GridExample(),
    );
  }
}

class GridExample extends StatelessWidget {
  const GridExample({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text("GridView.count Example")),
      body: GridView.count(
        crossAxisCount: 2, // Number of columns
        crossAxisSpacing: 10, // Horizontal space
        mainAxisSpacing: 10, // Vertical space
        padding: const EdgeInsets.all(10),
        children: List.generate(6, (index) {
          return Container(
            decoration: BoxDecoration(
              color: Colors.blueAccent,
              borderRadius: BorderRadius.circular(12),
            ),
            child: Center(
              child: Text(
                "Item $index",
                style: const TextStyle(color: Colors.white, fontSize: 18),
              ),
            ),
          );
        }),
      ),
    );
  }
}

⚙️ Key                     Properties
Property                Description
crossAxisCount            Number of columns in the grid.
mainAxisSpacing            Vertical spacing between rows.
crossAxisSpacing        Horizontal spacing between columns.
childAspectRatio        Controls item width/height ratio.
children                List of widgets displayed in the grid.
🎯 When to Use

Displaying product grids in e-commerce apps.

Creating a photo gallery.

Showing cards or categories in a dashboard.

Any UI with fixed number of columns.

⚖️ Comparison

GridView.count → Fixed number of columns (simpler).

GridView.builder → More efficient for large/dynamic lists.

GridView.extent → Fixes the maximum width of items instead of column count.
