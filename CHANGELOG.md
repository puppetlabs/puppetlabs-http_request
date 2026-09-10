# Changelog

## Release 1.0.0

### Breaking changes

* **Support Puppet 9 / Ruby 4** ([BOLT-193](https://perforce.atlassian.net/browse/BOLT-193))

  Migrates the module's dependency constraints and Ruby helper loading to work on the
  Puppet 9 / Ruby 4 runtime, in addition to existing Puppet 8 support. Major version
  bump reflects the runtime support change.

## Release 0.3.2

### New features

* **Bump ruby_task_helper upper bound to < 2.0.0** ([#18](https://github.com/puppetlabs/puppetlabs-http_request/pull/18))

## Release 0.3.1

### Bug fixes

- **Handle reponses without a body**
  ([#14](https://github.com/puppetlabs/puppetlabs-http_request/pull/14))

  The `http_request` task no longer errors when the response does not
  include a body.

  _Contributed by [op-ct](https://github.com/op-ct)._

## Release 0.3.0

### New features

- **Update `method` parameter to accept `patch`**
  ([#10](https://github.com/puppetlabs/puppetlabs-http_request/issues/10))

  The `method` parameter now accepts `patch` as a value.

  _Contributed by [op-ct](https://github.com/op-ct)._

## Release 0.2.2

### Bug fixes

- **Read key data from file passed to `key` parameter**
  ([#8](https://github.com/puppetlabs/puppetlabs-http_request/pull/8))

  Key data is now read from the file path passed to the `key` parameter.
  Previously, the file path itself was used as the key data.

## Release 0.2.1

### Bug fixes

- **Convert headers to strings**
  ([#4](https://github.com/puppetlabs/puppetlabs-http_request/pull/4))

  Headers set under the `headers` parameter are now converted to strings before
  making a request. Previously, headers were passed to the request as symbols.

  _Contributed by [barskern](https://github.com/barskern)._

## Release 0.2.0

### New features

- **Add `json_endpoint` parameter to `http_request` task**
  ([#2](https://github.com/puppetlabs/puppetlabs-http_request/issues/2))

  The `http_request` task now accepts a `json_endpoint` parameter. When set to
  `true`, the task will convert the request body to JSON, set the `Content-Type`
  header to `application/json`, and parse the response body as JSON.

## Release 0.1.0

This is the initial release.
