# Django For Professionals: Actual Database

The book now moves on from using the built in sqlite3 database to a proper database. We use a postgresql database to set up the database with docker-compose.

Now that we do everything through docker and docker-compose, it's a slightly more roundabout way of doing things that will result in eventually making deployment easier.

I have to install new packages in the docker image directly through docker-compose(after running docker-compose is up).

Then whenever a new package is installed, I have to build the image again with the new configurations.

I also have to create superusers through docker-compose as well. I guess this is sorta like working through a virtual machine but simpler?

I'm not sure if I got the terminology right.

There were some problems with the latest version(14 at the time of writing this readme) of postgres db not working properly with docker-compose(something about SCRAM authentication requiring libpq version 10 or above) but I got it working by downgrading to version 11 as shown in the book.

I may have to experiment with version 12 and 13 as well to see if those work with docker. I don't know if this is a M1 chip thing or a postgres thing or a docker thing. Googling hasn't been conclusive either. But I don't think it'll be a disaster to use slightly older versions of postgres.