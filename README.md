# WebDriver manager for java

[![](https://travis-ci.com/rosolko/wdm4j.svg?branch=master)](https://travis-ci.com/rosolko/wdm4j)
[![](https://sonarcloud.io/api/project_badges/measure?project=rosolko_wdm4j&metric=alert_status)](https://sonarcloud.io/dashboard?id=rosolko_wdm4j)
[![](https://sonarcloud.io/api/project_badges/measure?project=rosolko_wdm4j&metric=coverage)](https://sonarcloud.io/dashboard?id=rosolko_wdm4j)
[![](https://api.bintray.com/packages/rosolko/maven/wdm4j/images/download.svg)](https://bintray.com/rosolko/maven/wdm4j/_latestVersion)
[![](https://img.shields.io/maven-central/v/com.github.rosolko/wdm4j.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:%22com.github.rosolko%22%20AND%20a:%22wdm4j%22)

This small library aimed to automate the Selenium WebDriver binaries management inside a java project.

## Installation

    repositories {
        jcenter()
    }

	dependencies {
        implementation 'com.github.rosolko:wdm4j:1.0.0'
	}

## Using

**Pick preset binary configuration**:

* `ChromeConfig`
* `EdgeConfig`
* `FirefoxConfig`
* `InternetExplorerConfig`
* `OperaConfig`
* `PhantomJsConfig`

Or implement your own from `CommonConfig` interface

**Configure based on selected configuration**:

    new WebDriverManager().setup(new ChromeConfig())
    
**Lock binary version**:

    new WebDriverManager().setup(new ChromeConfig(), "2.45")    
