= Ruby on Rails 7.0 =

== Summary ==
Ruby on Rails 7.0 is the latest version of well known web framework written in Ruby.

== Owner ==
* Name: [[User:pvalena| Pavel Valena]], [[User:vondruch| Vít Ondruch]], [[User:jprokop| Jarek Prokop]]
* Email: pvalena@redhat.com, vondruch@redhat.com, jprokop@redhat.com, ruby-sig@lists.fedoraproject.org

== Current status ==
[[Category:ChangePageIncomplete]]
<!-- When your change proposal page is completed and ready for review and announcement -->
<!-- remove Category:ChangePageIncomplete and change it to Category:ChangeReadyForWrangler -->

[[Category:SelfContainedChange]]

* Targeted release: [[Releases/36 | Fedora 36 ]]
* Last updated: <!-- this is an automatic macro — you don't need to change this line -->  {{REVISIONYEAR}}-{{REVISIONMONTH}}-{{REVISIONDAY2}}
* FESCo issue: <will be assigned by the Wrangler>
* Tracker bug: <will be assigned by the Wrangler>
* Release notes tracker: <will be assigned by the Wrangler>

== Detailed Description ==
The Ruby on Rails stack is evolving quickly and Fedora needs to keep pace with it. Therefore the whole Ruby on Rails stack should be updated from 6.1 in Fedora 35 to 7.0 (latest version) in Fedora 36. This will ensure that all the Ruby developers using Fedora have the latest and greatest RPM-packaged Ruby on Rails.

== Benefit to Fedora ==
This update will keep Fedora up-to-date and will ensure that the current Ruby on Rails developers stay with us as they will get support for system-packaged Ruby on Rails of the latest version. Update to Rails 7.0 contains hundreds of fixes and improvements across all the frameworks. For new features, please see 'User Experience'.

== Scope ==
* Proposal owners:
** The whole Rails stack has to be updated.
** Some dependencies of the Rails stack will need update.

=== Packages need to be created/updated ===

* Bug: [https://bugzilla.redhat.com/show_bug.cgi?id=2032639 #2032639]

{|
! Package name
! Task
! Pull Request
|-
|rubygem-actioncable
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-actioncable/tree/rebase prepared git changes]
|-
|rubygem-actionmailbox
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-actionmailbox/tree/rebase prepared git changes]
|-
|rubygem-actionmailer
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-actionmailer/tree/rebase prepared git changes]
|-
|rubygem-actionpack
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-actionpack/tree/rebase prepared git changes]
|-
|rubygem-actiontext
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-actiontext/tree/rebase prepared git changes]
|-
|rubygem-actionview
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-actionview/tree/rebase prepared git changes]
|-
|rubygem-activejob
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-activejob/tree/rebase prepared git changes]
|-
|rubygem-activemodel
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-activemodel/tree/rebase prepared git changes]
|-
|rubygem-activerecord
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-activerecord/tree/rebase prepared git changes]
|-
|rubygem-activestorage
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-activestorage/tree/rebase prepared git changes]
|-
|rubygem-activesupport
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-activesupport/tree/rebase prepared git changes]
|-
|rubygem-rails
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-rails/tree/rebase prepared git changes]
|-
|rubygem-railties
|Update to 7.0.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-railties/tree/rebase prepared git changes]
|-
|rubygem-bootsnap
|Update to 1.10.x
|[https://src.fedoraproject.org/fork/pvalena/rpms/rubygem-bootsnap/tree/rebase prepared git changes]
|-
|rubygem-importmap-rails
|Newly packaged: [https://bugzilla.redhat.com/show_bug.cgi?id=2041471 BZ#2041471]
|[https://github.com/fedora-distgit/rubygem-importmap-rails prepared git changes]
|}

Current development state can be observed in [https://copr.fedorainfracloud.org/coprs/pvalena/ruby-on-rails/ pvalena/ruby-on-rails] COPR repository.
Current status: **version 7.0.0** built and tested

* Other developers: Update Rails dependent packages to be working with Ruby on Rails 7.0
* Policies and guidelines: N/A (not a System Wide Change)
* Trademark approval: N/A (not needed for this Change)

== Upgrade/compatibility impact ==
Web applications build above Ruby on Rails framework might need to be updated. Official upstream upgrade guide might come handy:
http://guides.rubyonrails.org/upgrading_ruby_on_rails.html

== How To Test ==
* No special hardware is needed.
* Some manual adjustments to dependencies are needed ([??? example]).

=== To test only Rails itself ===
<pre>
dnf install rubygem-rails
rails new app
cd app && rails s
</pre>
* Go to http://127.0.0.1:3000/ and make sure you are running Rails 7.0.x

=== To test the complete feature including generating a new Rails app using RPM ===
<pre>
dnf group install 'Ruby on Rails'
rails new app --skip-bundle && cd app
rails s
</pre>
* Go to http://127.0.0.1:3000/ and make sure you are running Rails 7.0.x

== User Experience ==
* New version of Ruby on Rails (7.0) available
* The most significant Rails 7.0 features:
** No-Node default approach to the front end
** Hotwire’s combination of Turbo and Stimulus
** Easily use any JavaScript bundler
** Encrypted attributes in Active Record
** Asynchronous Query Loading
** Zeitwerk autoloader is used exclusively

== Dependencies ==
* There are several packages, which depends on Ruby on Rails framework.
* These needs to be surely updated:
** (none)
* Following gems don't support Rails 7.0 right now and would be broken by the update:
** (none)
* As Rails requires Ruby >= 2.7, the platform less than the version can not use Rails 7.0.

== Contingency Plan ==
* Contingency mechanism: None needed. Rails stack won't be updated until all its dependencies are in Rawhide. After that, it will be a simple matter of updating the core packages (and their dependencies) via side-tag.
* Contingency deadline: N/A (not a System Wide Change)  <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
* Blocks release? No <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
* Blocks product? No <!-- Applicable for Changes that blocks specific product release/Fedora.next -->

== Documentation ==
* http://api.rubyonrails.org/

== Release Notes ==
https://rubyonrails.org/2021/12/15/Rails-7-fulfilling-a-vision
https://edgeguides.rubyonrails.org/7_0_release_notes.html
