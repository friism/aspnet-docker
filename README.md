# Supported tags

* [`latest` _(Dockerfile)_](1.0.0-beta1/Dockerfile)
* [`1.0.0-beta1` _(Dockerfile)_](1.0.0-beta1/Dockerfile)
* [`1.0.0-beta1-onbuild` _(Dockerfile)_](1.0.0-beta1/onbuild/Dockerfile)

# What is ASP.NET 5?

ASP.NET 5 is a lean .NET stack for building modern web apps. Microsoft built it from the ground up to provide an optimized development framework for apps that are either deployed to the cloud or run on-premises. It consists of modular components with minimal overhead, so you retain flexibility while constructing your solutions.

You can find more ASP.NET 5 resources here:

 * [ASP.NET 5 section on ASP.NET](http://www.asp.net/vnext)
 * [The Home directory in the ASP.NET GitHub org](https://github.com/aspnet/Home/)

![logo](https://github.com/friism/aspnet-docker/raw/master/logo.png)

# How to use this image

You can use the `onbuild` image to create images that run ASP.NET 5 web apps with the [Kestrel web server](https://github.com/aspnet/KestrelHttpServer), using Mono.

To run the [HelloWeb](https://github.com/aspnet/Home/tree/master/samples/HelloWeb) project from the ASP.NET 5 samples, place this Dockerfile in the HelloWeb project folder:

    FROM friism/aspnet-docker:1.0.0-beta1-onbuild

    EXPOSE 5004

Now build the image:

    docker build -t my-app .

Finally run your app:

    docker run -t -p 80:5004 my-app

The HelloWeb site will now be available on port 80 on your machine.

# Issues

Please report issues on the [GitHub project](https://github.com/friism/aspnet-docker).

# License

This Docker image is licensed with the MIT license.
