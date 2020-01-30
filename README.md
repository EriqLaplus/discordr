
# discordr - A set of utility functions for interaction with Discord through R and RStudio

<!-- badges: start -->
<!-- badges: end -->

The goal of discordr is to make writing bots and collaborating in Discord easier through a set of utility functions.

## Installation

You can install the released version of discordr from Github with:

``` r
library(devtools)
install_github("EriqLaplus/discordr")
```

## Setup

This packages functions through Discord's easy-to-use webhook system. If you are the owner or administrator of a channel, you can setup a webhook by entering the channel settings (edit channel) and navigating to the webhook tab. If you are the participant of a channel, you may request a webhook from an administator in order to use this package. While not required, it is recommended to set a default username and webhook for easier use.

``` r
library(discordr)

set_discordr_username("dataman")
set_discordr_webhook("https://discord.com/your-webhook-here")
```

## Examples

Once setup, there are three primary ways to interact with Discord through this package: sending messages, sending files, and sending the current plot from RStudio. For sending messages, use the `send_message` function with a character string. See package documentation if you are not setting a default username and/or default webhook

``` r
send_message("Hello World!")
```
For sending files, user the `send_file` function with the filepath as a character string.

``` r
send_file("hello_world.jpg")
send_file("updated_dataset.csv")
```

Finally, you can use the `send_current_plot` or `send_current_ggplot` functions to send the last plot shown in the Plots tab of RStudio. If using a ggplot workflow, using the appropriate `send_current_ggplot` function is recommended to obtain the highest image resolution.

``` r
send_current_ggplot()
```

