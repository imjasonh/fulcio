# v0.2.0

## Enhancements

* Use fulcio-system ns and drop -dev suffix for sa (https://github.com/sigstore/fulcio/pull/418)
* Return an error if we fail get get the Root cert. (https://github.com/sigstore/fulcio/pull/416)
* Add unit tests for oidc-EmailFromIDToken method (https://github.com/sigstore/fulcio/pull/413)
* extract CA/KMS support info to separate file (https://github.com/sigstore/fulcio/pull/409)
* add securityContext to deployment (https://github.com/sigstore/fulcio/pull/420)
* Count HTTP request error codes with prometheus (https://github.com/sigstore/fulcio/pull/396)
* Remove organization from subject for GCP CAS issuer (https://github.com/sigstore/fulcio/pull/391)
* Update warning text. (https://github.com/sigstore/fulcio/pull/389)
* Improve error messages returned by SigningCert (https://github.com/sigstore/fulcio/pull/388)
* Allow parameterized application/json content types (https://github.com/sigstore/fulcio/pull/386)
* Add AKS MetaIssuer (https://github.com/sigstore/fulcio/pull/384)
* Move CTL logging logic over to CTL package (https://github.com/sigstore/fulcio/pull/353)
* Move OID information to docs directory and reformat (https://github.com/sigstore/fulcio/pull/378)
* Upgrade miekg/pkcs11 using 'go get github.com/miekg/pkcs11@v1.1.1' (https://github.com/sigstore/fulcio/pull/376)
* Address signingCert panic with the last-byte calculation of finalChainPEM (https://github.com/sigstore/fulcio/pull/370)
* Include instructions to download verify the fulcio root certificate with TUF (https://github.com/sigstore/fulcio/pull/361)
* Make CA explicit dependency of API handler (https://github.com/sigstore/fulcio/pull/354)
* Improve error message when an invalid OIDC issuer is provided (https://github.com/sigstore/fulcio/pull/357)
* Make the the invalid CA error message actionable (https://github.com/sigstore/fulcio/pull/356)
* Initialize CT log client once (https://github.com/sigstore/fulcio/pull/350)
* Generate subject key ID correctly for non-GCP certs (https://github.com/sigstore/fulcio/pull/345)
* Add chain in response for all CAs, fix newlines in response (https://github.com/sigstore/fulcio/pull/341)
* Add some reasonable timeouts to API server (https://github.com/sigstore/fulcio/pull/337)
* fileca: add support for intermediate certificates (https://github.com/sigstore/fulcio/pull/320)
* Set max request size to 4MiB (https://github.com/sigstore/fulcio/pull/338)
* Extract additional claims  from github-workflow token (https://github.com/sigstore/fulcio/pull/306)
* Enable server settings via config file and env vars (https://github.com/sigstore/fulcio/pull/315)
* Add file backed certificate authority (https://github.com/sigstore/fulcio/pull/280)
* Handle error when there are no roots returned by CA Service (https://github.com/sigstore/fulcio/pull/298)
* Add RootCert method to client + tests (https://github.com/sigstore/fulcio/pull/290)
* Add back support for building with CGO_ENABLED=0 (https://github.com/sigstore/fulcio/pull/293)
* add usersnames list to the codeonwers to make it easier to check (https://github.com/sigstore/fulcio/pull/295)
* Add a Root Cert method to the CA interface, and implement it. (https://github.com/sigstore/fulcio/pull/287)
* Update readme for V1 CA Service (https://github.com/sigstore/fulcio/pull/286)
* Fail fast if private key is not found when using PKCS11 CA (https://github.com/sigstore/fulcio/pull/285)
* Do not close the PKCS11 context on startup (https://github.com/sigstore/fulcio/pull/282)
* Localize flags to each subcommand (https://github.com/sigstore/fulcio/pull/274)
* Make client request timeout configurable with `WithTimeout` client option (https://github.com/sigstore/fulcio/pull/272)
* add the ability to set the user-agent string on requests from the `Client` (https://github.com/sigstore/fulcio/pull/264)
* Consolidate the source-of-truth. (https://github.com/sigstore/fulcio/pull/263)
* Move the deployment to the new v1 cert. (https://github.com/sigstore/fulcio/pull/261)
* The v1 GCP CA requires this field to be set. (https://github.com/sigstore/fulcio/pull/260)
* Experiment with FulcioConfig pulling from context.Context (https://github.com/sigstore/fulcio/pull/249)
* Upgrade fulcios to use of the google privateca api at v1 (https://github.com/sigstore/fulcio/pull/218)
* plumb through !cgo golang tags that removes pkcs11 support (https://github.com/sigstore/fulcio/pull/244)
* break out CA-specific implementation from common API class (https://github.com/sigstore/fulcio/pull/220)
* Add support for recoginizing allow.pub as an spiffe issuer (https://github.com/sigstore/fulcio/pull/228)
* Various nits trying SoftHSM (https://github.com/sigstore/fulcio/pull/217)
* Use MetaIssuers to simular EKS / GKE in e2e test. (https://github.com/sigstore/fulcio/pull/225)
* Add support for "meta issuers". (https://github.com/sigstore/fulcio/pull/223)
* Remove the cluster-local block by default. (https://github.com/sigstore/fulcio/pull/224)
* Refactor the way we access `Config` (https://github.com/sigstore/fulcio/pull/222)
* Enable Fulcio e2e testing. (https://github.com/sigstore/fulcio/pull/219)
* use sigstore/sigstore instead of directly calling RSA/ECDSA verify calls (https://github.com/sigstore/fulcio/pull/221)
* Refactor the kind e2e test. (https://github.com/sigstore/fulcio/pull/215)
* Add issuer information to code signing certificates (https://github.com/sigstore/fulcio/pull/204)
* Extract the OIDC issuer URL. (https://github.com/sigstore/fulcio/pull/211)
* use request ID logger where possible (https://github.com/sigstore/fulcio/pull/209)
* Rewrite "FulcioCA" to "PKCS11CA" and add AWS support (https://github.com/sigstore/fulcio/pull/187)
* add pkcs11-config-path command line parameter (https://github.com/sigstore/fulcio/pull/192)
* Add GitHub OIDC to Fulcio (https://github.com/sigstore/fulcio/pull/181)
* Changes fulcio-server to fulcio (https://github.com/sigstore/fulcio/pull/186)
* Add Github to `fulcioca` path. (https://github.com/sigstore/fulcio/pull/184)
* Add support for Github OIDC (https://github.com/sigstore/fulcio/pull/180)
* Generate client code with swagger in Makefile (https://github.com/sigstore/fulcio/pull/176)
* Switch to the JSON logger in prod (https://github.com/sigstore/fulcio/pull/175)
* add SCT as HTTP response header (https://github.com/sigstore/fulcio/pull/163)
* fulcio: add version command (https://github.com/sigstore/fulcio/pull/155)
* Script and process to generate OIDC config from federation directory. (https://github.com/sigstore/fulcio/pull/139)


## Bug Fixes

* Fix the SCT header return value from the API to base64 encode it. (https://github.com/sigstore/fulcio/pull/288)
* Fix the k8s subject parsing. (https://github.com/sigstore/fulcio/pull/254)
* [Correction] Upgrade fulcios to use of the google privateca api at v1 (https://github.com/sigstore/fulcio/pull/252)
* fix: go get complain missing version when dir not in module (https://github.com/sigstore/fulcio/pull/248)
* Fix street-address and postal-code descriptions to be more descriptive. (https://github.com/sigstore/fulcio/pull/245)
* fix cutpaste error, sets cpu correctly (https://github.com/sigstore/fulcio/pull/237)
* Fix nil pointer, update dev docs (https://github.com/sigstore/fulcio/pull/236)
* Fix the Github OIDC challenge endpoint (https://github.com/sigstore/fulcio/pull/206)
* Fix misspellings. (https://github.com/sigstore/fulcio/pull/177)

## Documentation

* extract development documentation from README (https://github.com/sigstore/fulcio/pull/410)
* fixing link to external resources (https://github.com/sigstore/fulcio/pull/411)
* Add feature stability and deprecation docs (https://github.com/sigstore/fulcio/pull/400)
* docs: overview of certificate issuing (https://github.com/sigstore/fulcio/pull/383)
* Add Logo to README (https://github.com/sigstore/fulcio/pull/381)
* Move sec model out of readme (https://github.com/sigstore/fulcio/pull/382)
* Update README for V1 Fulcio cert (https://github.com/sigstore/fulcio/pull/355)
* fix link for SECURITY.md (https://github.com/sigstore/fulcio/pull/340)
* Remove root CA whitespaces on README.md (https://github.com/sigstore/fulcio/pull/325)
* Add Locust load test and README (https://github.com/sigstore/fulcio/pull/311)
* add oid documentation (https://github.com/sigstore/fulcio/pull/307)
* Add documentation for testing with `ephemeralca` as well as document (https://github.com/sigstore/fulcio/pull/296)

## Others

* Bump actions/upload-artifact from 2.3.1 to 3 (https://github.com/sigstore/fulcio/pull/452)
* Go update to 1.17.8 and cosign to 1.6.0 (https://github.com/sigstore/fulcio/pull/453)
* add missing target name (https://github.com/sigstore/fulcio/pull/450)
* Bump cloud.google.com/go/security from 1.2.1 to 1.3.0 (https://github.com/sigstore/fulcio/pull/448)
* Bump golang from `c2ca472` to `b983574` (https://github.com/sigstore/fulcio/pull/447)
* Move CI private-ca YAML to subdir (https://github.com/sigstore/fulcio/pull/446)
* Add step in release to mirror signed image to ghcr (https://github.com/sigstore/fulcio/pull/441)
* Bump actions/checkout from 2 to 3 (https://github.com/sigstore/fulcio/pull/443)
* Bump golang from `e06c834` to `c2ca472` (https://github.com/sigstore/fulcio/pull/442)
* Bump actions/setup-go from 2.2.0 to 3.0.0 (https://github.com/sigstore/fulcio/pull/440)
* Bump golangci/golangci-lint-action from 3.0.0 to 3.1.0 (https://github.com/sigstore/fulcio/pull/439)
* Bump golangci/golangci-lint-action from 2.5.2 to 3 (https://github.com/sigstore/fulcio/pull/438)
* Bump github/codeql-action from 1.1.2 to 1.1.3 (https://github.com/sigstore/fulcio/pull/435)
* Bump github.com/magiconair/properties from 1.8.5 to 1.8.6 (https://github.com/sigstore/fulcio/pull/436)
* add indent to fix yaml error (https://github.com/sigstore/fulcio/pull/434)
* Bump cloud.google.com/go/security from 1.2.0 to 1.2.1 (https://github.com/sigstore/fulcio/pull/431)
* explicitly set permissions for github workflows (https://github.com/sigstore/fulcio/pull/433)
* Bump google.golang.org/api from 0.69.0 to 0.70.0 (https://github.com/sigstore/fulcio/pull/432)
* Add missing testing dependency (https://github.com/sigstore/fulcio/pull/429)
* Workflow to kick off release. (https://github.com/sigstore/fulcio/pull/407)
* Take advantage of Chainguard maintained versions of various actions. (https://github.com/sigstore/fulcio/pull/427)
* Bump golang from `2c92978` to `e06c834` (https://github.com/sigstore/fulcio/pull/426)
* create namespace as part of config yaml (https://github.com/sigstore/fulcio/pull/422)
* Bump golang from `1a35cc2` to `2c92978` (https://github.com/sigstore/fulcio/pull/423)
* Bump ossf/scorecard-action from 1.0.3 to 1.0.4 (https://github.com/sigstore/fulcio/pull/425)
* Bump github/codeql-action from 1.1.0 to 1.1.2 (https://github.com/sigstore/fulcio/pull/424)
* Bump google.golang.org/api from 0.68.0 to 0.69.0 (https://github.com/sigstore/fulcio/pull/412)
* Bump cloud.google.com/go/security from 1.1.1 to 1.2.0 (https://github.com/sigstore/fulcio/pull/408)
* Bump github/codeql-action from 1.0.32 to 1.1.0 (https://github.com/sigstore/fulcio/pull/406)
* update cross-build to use go 1.17.7 (https://github.com/sigstore/fulcio/pull/404)
* Bump golang from 1.17.6 to 1.17.7 (https://github.com/sigstore/fulcio/pull/403)
* Bump golang from `301609e` to `fff998d` (https://github.com/sigstore/fulcio/pull/401)
* Bump actions/setup-go from 2.1.5 to 2.2.0 (https://github.com/sigstore/fulcio/pull/402)
* Bump google.golang.org/api from 0.67.0 to 0.68.0 (https://github.com/sigstore/fulcio/pull/399)
* Bump go.uber.org/zap from 1.20.0 to 1.21.0 (https://github.com/sigstore/fulcio/pull/393)
* Bump github/codeql-action from 1.0.31 to 1.0.32 (https://github.com/sigstore/fulcio/pull/392)
* Bump google.golang.org/api from 0.66.0 to 0.67.0 (https://github.com/sigstore/fulcio/pull/385)
* Bump github/codeql-action from 1.0.30 to 1.0.31 (https://github.com/sigstore/fulcio/pull/366)
* Bump ossf/scorecard-action from 1.0.2 to 1.0.3 (https://github.com/sigstore/fulcio/pull/367)
* Bump go.step.sm/crypto from 0.15.0 to 0.15.1 (https://github.com/sigstore/fulcio/pull/377)
* Bump google.golang.org/api from 0.65.0 to 0.66.0 (https://github.com/sigstore/fulcio/pull/363)
* Bump github.com/prometheus/client_golang from 1.12.0 to 1.12.1 (https://github.com/sigstore/fulcio/pull/362)
* Bump golang from `d7f2f6f` to `301609e` (https://github.com/sigstore/fulcio/pull/358)
* Bump go.step.sm/crypto from 0.14.0 to 0.15.0 (https://github.com/sigstore/fulcio/pull/359)
* Bump golang from `0fa6504` to `d7f2f6f` (https://github.com/sigstore/fulcio/pull/352)
* createca: Address panic when no private key pair matches (https://github.com/sigstore/fulcio/pull/351)
* update version marker (https://github.com/sigstore/fulcio/pull/346)
* Remove Google CA v1beta1 API and associated config (https://github.com/sigstore/fulcio/pull/349)
* Bump ossf/scorecard-action from 1.0.1 to 1.0.2 (https://github.com/sigstore/fulcio/pull/347)
* update to v1.0.29 of codeql-action (https://github.com/sigstore/fulcio/pull/344)
* Bump github.com/prometheus/client_golang from 1.11.0 to 1.12.0 (https://github.com/sigstore/fulcio/pull/333)
* Bump github.com/google/go-cmp from 0.5.6 to 0.5.7 (https://github.com/sigstore/fulcio/pull/334)
* Update github/codeql-action requirement to 8a4b243fbf9a03a93e93a71c1ec257347041f9c4 (https://github.com/sigstore/fulcio/pull/332)
* Bump ossf/scorecard-action from 0fe1afdc40f536c78e3dc69147b91b3ecec2cc8a to 1.0.1 (https://github.com/sigstore/fulcio/pull/331)
* pin one additional set of actions (https://github.com/sigstore/fulcio/pull/329)
* Bump google.golang.org/api from 0.64.0 to 0.65.0 (https://github.com/sigstore/fulcio/pull/321)
* add OSSF scorecard action (https://github.com/sigstore/fulcio/pull/328)
* Bump golang from `8c0269d` to `0fa6504` (https://github.com/sigstore/fulcio/pull/326)
* pin github actions by digest instead of tag (https://github.com/sigstore/fulcio/pull/323)
* release: add cloudbuild to run the release for fulcio (https://github.com/sigstore/fulcio/pull/322)
* Fix docker-compose dexidp startup (https://github.com/sigstore/fulcio/pull/316)
* Bump go.step.sm/crypto from 0.13.0 to 0.14.0 (https://github.com/sigstore/fulcio/pull/319)
* Bump golang from 1.17.5 to 1.17.6 (https://github.com/sigstore/fulcio/pull/317)
* Switch to use fileca in e2e tests (https://github.com/sigstore/fulcio/pull/309)
* Bump google.golang.org/api from 0.63.0 to 0.64.0 (https://github.com/sigstore/fulcio/pull/318)
* Remove hack/tools (https://github.com/sigstore/fulcio/pull/308)
* Bump cloud.google.com/go/security from 1.1.0 to 1.1.1 (https://github.com/sigstore/fulcio/pull/312)
* Bump go.uber.org/zap from 1.19.1 to 1.20.0 (https://github.com/sigstore/fulcio/pull/313)
* Bump github.com/sigstore/sigstore from 1.0.1 to 1.1.0 (https://github.com/sigstore/fulcio/pull/299)
* Change ports for docker compose to avoid conflict with Rekor (https://github.com/sigstore/fulcio/pull/297)
* Bump github.com/spf13/viper from 1.10.0 to 1.10.1 (https://github.com/sigstore/fulcio/pull/283)
* Bump github.com/spf13/cobra from 1.2.1 to 1.3.0 (https://github.com/sigstore/fulcio/pull/278)
* Bump golang from 1.17.4 to 1.17.5 (https://github.com/sigstore/fulcio/pull/269)
* Bump github.com/prometheus/common from 0.29.0 to 0.32.1 (https://github.com/sigstore/fulcio/pull/270)
* Bump golang from 1.17.3 to 1.17.4 (https://github.com/sigstore/fulcio/pull/265)
* Wrap the server with the Prometheus so we get metrics + add an e2e te… (https://github.com/sigstore/fulcio/pull/267)
* While working on #267 noticed this, but didn't want to bake into it. (https://github.com/sigstore/fulcio/pull/268)
* Drop OpenAPI from Fulcio (https://github.com/sigstore/fulcio/pull/262)
* Drop useless package. (https://github.com/sigstore/fulcio/pull/259)
* Drop gratuitous `sync.Once` in google CAs. (https://github.com/sigstore/fulcio/pull/258)
* Remove `viper` from `pkg/`. (https://github.com/sigstore/fulcio/pull/257)
* Bump github.com/mitchellh/mapstructure from 1.4.2 to 1.4.3 (https://github.com/sigstore/fulcio/pull/256)
* Consolidate `viper` usage in `pkg/ca/ca.go` (https://github.com/sigstore/fulcio/pull/255)
* Bump cloud.google.com/go/security from 0.1.0 to 1.1.0 (https://github.com/sigstore/fulcio/pull/246)
* Bump github.com/go-openapi/strfmt from 0.21.0 to 0.21.1 (https://github.com/sigstore/fulcio/pull/247)
* Use `CGO_ENABLED=1` via `.ko.yaml`. (https://github.com/sigstore/fulcio/pull/242)
* Bump github.com/sigstore/sigstore from 1.0.0 to 1.0.1 (https://github.com/sigstore/fulcio/pull/239)
* Add commit sha and trigger to github workflow (https://github.com/sigstore/fulcio/pull/232)
* Bump golang from 1.17.2 to 1.17.3 (https://github.com/sigstore/fulcio/pull/234)
* Bump actions/checkout from 2.3.5 to 2.4.0 (https://github.com/sigstore/fulcio/pull/233)
* Bump github.com/go-openapi/runtime from 0.20.0 to 0.21.0 (https://github.com/sigstore/fulcio/pull/229)
* Bump github.com/go-openapi/strfmt from 0.20.3 to 0.21.0 (https://github.com/sigstore/fulcio/pull/226)
* Bump github.com/hashicorp/golang-lru from 0.5.3 to 0.5.4 (https://github.com/sigstore/fulcio/pull/227)
* bump go-swagger to v0.28.0 (https://github.com/sigstore/fulcio/pull/213)
* Reproducible builds with trimpath (https://github.com/sigstore/fulcio/pull/210)
* Bump actions/checkout from 2.3.4 to 2.3.5 (https://github.com/sigstore/fulcio/pull/207)
* Bump github.com/go-openapi/runtime from 0.19.31 to 0.20.0 (https://github.com/sigstore/fulcio/pull/202)
* Bump github.com/go-openapi/spec from 0.20.3 to 0.20.4 (https://github.com/sigstore/fulcio/pull/201)
* Bump github.com/go-openapi/validate from 0.20.2 to 0.20.3 (https://github.com/sigstore/fulcio/pull/198)
* update go.sum (https://github.com/sigstore/fulcio/pull/205)
* Bump github.com/go-openapi/loads from 0.20.2 to 0.20.3 (https://github.com/sigstore/fulcio/pull/200)
* Bump github.com/go-openapi/strfmt from 0.20.2 to 0.20.3 (https://github.com/sigstore/fulcio/pull/199)
* Bump golang from 1.17.1 to 1.17.2 (https://github.com/sigstore/fulcio/pull/197)
* Bump github.com/spf13/viper from 1.8.1 to 1.9.0 (https://github.com/sigstore/fulcio/pull/189)
* Bump github.com/coreos/go-oidc/v3 from 3.0.0 to 3.1.0 (https://github.com/sigstore/fulcio/pull/188)
* Bump github.com/mitchellh/mapstructure from 1.4.1 to 1.4.2 (https://github.com/sigstore/fulcio/pull/185)
* Bump github.com/ThalesIgnite/crypto11 from 1.2.4 to 1.2.5 (https://github.com/sigstore/fulcio/pull/182)
* Bump golang from 1.17.0 to 1.17.1 (https://github.com/sigstore/fulcio/pull/179)
* Bump go.uber.org/zap from 1.19.0 to 1.19.1 (https://github.com/sigstore/fulcio/pull/178)
* Bump github.com/go-openapi/runtime from 0.19.30 to 0.19.31 (https://github.com/sigstore/fulcio/pull/171)
* Bump github.com/go-openapi/errors from 0.20.0 to 0.20.1 (https://github.com/sigstore/fulcio/pull/169)
* Bump github.com/go-openapi/strfmt from 0.20.1 to 0.20.2 (https://github.com/sigstore/fulcio/pull/168)
* Bump golang from 1.16.7 to 1.17.0 (https://github.com/sigstore/fulcio/pull/166)
* Bump cloud.google.com/go from 0.91.1 to 0.92.3 (https://github.com/sigstore/fulcio/pull/167)
* Bump cloud.google.com/go from 0.90.0 to 0.91.1 (https://github.com/sigstore/fulcio/pull/162)
* Bump github.com/go-openapi/runtime from 0.19.29 to 0.19.30 (https://github.com/sigstore/fulcio/pull/161)
* Bump go.uber.org/zap from 1.18.1 to 1.19.0 (https://github.com/sigstore/fulcio/pull/160)
* Bump golang from 1.16.6 to 1.16.7 (https://github.com/sigstore/fulcio/pull/159)
* Bump cloud.google.com/go from 0.89.0 to 0.90.0 (https://github.com/sigstore/fulcio/pull/158)
* Bump cloud.google.com/go from 0.88.0 to 0.89.0 (https://github.com/sigstore/fulcio/pull/156)
* makefile: add rule to download and set swagger and make rule to build the dist (https://github.com/sigstore/fulcio/pull/154)
* Add missing code of conduct (stock sigstore one) (https://github.com/sigstore/fulcio/pull/153)

## Contributors

* Appu (@loosebazooka)
* Asra Ali (@asraa)
* Bob Callaway (@bobcallaway)
* Carlos Tadeu Panato Junior (@cpanato)
* Christian Kotzbauer (@ckotzbauer)
* Dan Lorenc (@dlorenc)
* Elizabeth Thomas (@elizabetht)
* Evan Phoenix (@evanphx)
* Hayden Blauzvern (@haydentherapper)
* Jake Sanders (@dekkagaijin)
* Josh Dolitsky (@jdolitsky)
* Jyotsna (@jyotsna-penumaka)
* Kenny Leung (@k4leung4)
* Luke Hinds (@lukehinds)
* Mark Bestavros (@mbestavros)
* Matt Moore (@mattmoor)
* Matthew Suozzo (@msuozzo)
* Nathan Smith (@nsmith5)
* Naveen (@naveensrinivasan)
* Nghia Tran (@tcnghias)
* Priya Wadhwa (@priyawadhwa)
* Radoslav Gerganov (@rgerganov)
* Rafael Fernández López (@ereslibre)
* Scott Nichols (@n3wscott)
* Thomas Strömberg (@tstromberg)
* Tuan Anh Tran (@tuananh)
* Viacheslav Vasilyev (@avoidik)
* Ville Aikas (@vaikas)
* Zack Newman (@znewman01)
* endorama (@endorama)
