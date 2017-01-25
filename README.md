## Basic Docker Container

### Disclaimer

This docker image is far from being truly persistent and docker-way. It is more like a beginning to start an evolved container but it is a good way to start.





### Supported tags and respective Dockerfile links
I've worked to automate as soon this image using this [Dockerfile](https://github.com/starase/base)


### Details
Image: Ubuntu 16.04 LTS
Process control system: supervisord

*Image size: ~380Mb*

### Software
* vim
* supervisor
* oh-my-zsh (by default)

I have customized the default template of zsh's shell
I have changed:

- default theme (I'm using darkblood);
- disable prompt update;
- automatic updates (updates every 7 days, of course you can change this parameter);
- locale (en_US.UTF-8);

### Try it
You can pull the image and it will be up&running simply doing:

``` docker pull starase/base ```

You can start it:

```docker run -d -i -t starase/base /usr/bin/supervisord -n -c /etc/supervisor/supervisord.conf```

Of course you can customize it. 
For istance you can put name or hostname, simply adding ```--name name``` and ```--h hostname``` before the image's name




### Issues & Contributing
Before you start to code, we recommend discussing your plans through a GitHub issue, especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing. Otherwise you feel free to drop me a line at paolo [at] starase.com


> Have fun, happy dockerizing
