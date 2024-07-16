# hadoop-examples-mapreduce


# Hadoop MapReduce Examples

This repository contains examples of MapReduce jobs implemented in Java for processing data with Apache Hadoop. 

## Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Setup](#setup)
- [Upload the dataset to HDFS](#upload-the-dataset-to-hdfs)
- [Running the Jobs](#running-the-jobs)
- [Unit Tests](#unit-tests)

## Overview

This project demonstrates several MapReduce jobs including:
- Listing distinct districts containing trees
- Showing all existing species
- Counting the number of trees by kind
- Calculating the maximum height per kind of tree

## Requirements

- Java 8
- Apache Hadoop 3.x
- Maven 3.x
- Git


## Upload the dataset to HDFS

Ensure you have the dataset `trees.csv` in your local directory. Then, upload it to HDFS in FileZilla:

## Running the jobs
Voici le contenu du fichier `README.md` en Markdown avec les sections bien formatées pour être copié directement dans votre fichier :

```markdown
# Hadoop MapReduce Examples

This repository contains examples of MapReduce jobs implemented in Java for processing data with Apache Hadoop.

## Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Setup](#setup)
- [Running the Jobs](#running-the-jobs)
  - [Districts Containing Trees](#districts-containing-trees)
  - [Existing Species](#existing-species)
  - [Number of Trees by Kind](#number-of-trees-by-kind)
  - [Maximum Height per Kind of Tree](#maximum-height-per-kind-of-tree)
- [Unit Tests](#unit-tests)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project demonstrates several MapReduce jobs including:
- Listing distinct districts that contain trees
- Showing all existing species
- Counting the number of trees by kind
- Calculating the maximum height per kind of tree

## Requirements

- Java 8
- Apache Hadoop 3.x
- Maven 3.x
- Git


2. **Build the project using Maven:**

   ```sh
   mvn clean package -DskipTests
   ```

3. **Upload the dataset to HDFS:**

   Ensure you have the dataset `trees.csv` in your local directory. Then, upload it using Filezilla
   ```

## Running the Jobs

### Districts Containing Trees

This job lists distinct districts that contain trees.

1. **Run the job:**

   ```sh
   yarn jar /home/<username>/hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar com.opstty.job.District /user/<username>/trees/trees.csv /user/<username>/output_districts
   ```

2. **Check the output:**

   ```sh
   hdfs dfs -cat /user/<username>/output_districts/part-r-00000
   ```

### Existing Species

This job displays the list of different species trees in the file.

1. **Run the job:**

   ```sh
   yarn jar /home/<username>/hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar com.opstty.job.Species /user/<username>/trees/trees.csv /user/<username>/output_species
   ```

2. **Check the output:**

   ```sh
   hdfs dfs -cat /user/<username>/output_species/part-r-00000
   ```

### Number of Trees by Kind

This job calculates the number of trees of each kind.

1. **Run the job:**

   ```sh
   yarn jar /home/<username>/hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar com.opstty.job.Treeskind /user/<username>/trees/trees.csv /user/<username>/output_treeskind
   ```

2. **Check the output:**

   ```sh
   hdfs dfs -cat /user/<username>/output_treeskind/part-r-00000
   ```

### Maximum Height per Kind of Tree

This job calculates the height of the tallest tree of each kind.

1. **Run the job:**

   ```sh
   yarn jar /home/<username>/hadoop-examples-mapreduce-1.0-SNAPSHOT-jar-with-dependencies.jar com.opstty.job.Maxheightkind /user/<username>/trees/trees.csv /user/<username>/output_maxheight
   ```

2. **Check the output:**

   ```sh
   hdfs dfs -cat /user/<username>/output_maxheight/part-r-00000
   ```

