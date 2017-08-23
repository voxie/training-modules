# Introduction

Packer is a critical component of our infrastructure as code paradigm. The 
tldr is that packer is a tool that allows you to create machine images 
across cloud providers using json.

The best way to get started with packer is to work through their 
documentation:

* [Packer](https://www.packer.io/intro/hashicorp-ecosystem.html)

The Test:

1. Create an ami on amazon using Ubuntu as the base image id of: ami-cd0f5cb6
2. Make sure that nginx is installed on the image