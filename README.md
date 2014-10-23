autoping-play2-plugin
=====================

build.sbt : 

import play.PlayScala

name := "test"

version := "1.0-SNAPSHOT"

lazy val root = (project in file(".")).enablePlugins(PlayScala)

libraryDependencies ++= Seq(
  ws,
  "com.github.ndeverge" %% "autoping-play2-plugin" % "0.1.2"
)

resolvers ++= Seq(
  "Typesafe repository" at "http://repo.typesafe.com/typesafe/releases/",
  "Sonatype snapshots" at "https://oss.sonatype.org/content/repositories/snapshots",
  Resolver.url("My GitHub Play Repository", url("http://github.com/juliender/autoping-play2-plugin/snapshots/"))(Resolver.ivyStylePatterns)
)
