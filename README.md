# NAME

Plack::Middleware::Matomo - a middleware to track usage information with Matomo

# SYNOPSIS

    builder {
        enable "Plack::Middleware::Matomo",
            id_site => "my-service",
            base_url => "https://somewhere.eu/matomo",
            auth_token => "secr3t",
            view_paths => ['record/(\w+)/*'],
            download_paths => ['download/(\w+)/*'],
            oai_identifier_format => 'oai:test.server.org:%s',
            ;
        $app;
    }

# CONFIGURATION

- id\_site

    Required. The ID of the repository.

- base\_url

    Required. The URL of the Matomo endpoint.

- auth\_token

    Required. The authorization token.

- view\_paths, download\_paths

    One of these is required. Provide an array ref of regexes to match.

- oai\_identifier\_format

    Required. The format of the OAI identifier format of the repository.

# DESCRIPTION

tbd.

# AUTHOR

Vitali Peil &lt;vitali.peil at uni-bielefeld.de>

# COPYRIGHT

Copyright 2019- Vitali Peil

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO

[Plack::Middleware](https://metacpan.org/pod/Plack::Middleware), [Plack::Builder](https://metacpan.org/pod/Plack::Builder)
