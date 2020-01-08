# forums.naturalcapitalproject.org
Redirect to the discourse-powered https://community.naturalcapitalproject.org

We discovered on 2020-01-08 that Google searches for the phrase "natcap forums invest" were
returning results to the old forums site, https://forums.naturalcapitalproject.org.  In
fact, the old `forums` subdomain was the top hit.

The original workaround for this was to create a GCS bucket with the `forums` subdomain
and just redirect all traffic to the new domain.  The unfortunate shortcoming of this
is that hosting static sites on GCS does not support HTTPS ... and the google search
results were for an HTTPS subdomain.  Queue scary error.

This repo is an attempt to host this single, static `index.html` page right here
on github's infrastructure (which DOES serve things over HTTPS if we ask nicely)
and get around the scary warning.

Feel free to remove or archive this repo once the old forums subdomain is no longer
the top hit.
