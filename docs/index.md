# Moonshot
_Because releasing services shouldn't be a moonshot._

## Overview

Moonshot is a Ruby gem for provisioning environments in AWS using a CLI.
The environments are centered around a single CloudFormation stack and supported
by pluggable systems:
- A DeploymentMechanism controls releasing code.
- A BuildMechanism creates a release artifact.
- A ArtifactRepository stores the release artifacts.

## Design Goals

These are core ideas to the creation of this project. Not all are met to the
level we'd like (e.g. CloudFormation isn't much of a Choice currently), but we
should aspire to meet them with each iteration.

- Simplicity: It shouldn't take more than a few hours to understand what your
  release tooling does.
- Choice: As much as possible, each component should be pluggable and omittable,
  so teams are free to use what works best for them.
- Verbosity: The output of core Moonshot code should explain in detail what
  changes are being made, so knowledge is shared and not abstracted.

## Installation

Add this line to your application's Gemfile:

    gem 'moonshot'

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install moonshot


## Getting started

The Moonshot tool has been designed to be an extensible library for your specific use-case. Interested in how it can be used? See our [example](example.md) documentation or look at our [sample application](https://github.com/acquia/moonshot-sample-app)

## Requirements

- Ruby 2.1 or higher
