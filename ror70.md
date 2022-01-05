= Ruby on Rails 6.1 =

== Summary ==
Ruby on Rails 6.1 is the latest version of well known web framework written in Ruby.

== Owner ==
* Name: [[User:pvalena| Pavel Valena]], [[User:vondruch| Vít Ondruch]], [[User:jaruga| Jun Aruga]]
* Email: pvalena@redhat.com, vondruch@redhat.com, jaruga@redhat.com, ruby-sig@lists.fedoraproject.org
<!--- UNCOMMENT only for Changes with assigned Shepherd (by FESCo)
* FESCo shepherd: [[User:FASAccountName| Shehperd name]] <email address>
-->
<!--- UNCOMMENT only if this Change aims specific product, working group (Cloud, Workstation, Server, Base, Env & Stacks)
* Product:
* Responsible WG:
-->

== Current status ==
[[Category:ChangeAcceptedF34]]
<!-- When your change proposal page is completed and ready for review and announcement -->
<!-- remove Category:ChangePageIncomplete and change it to Category:ChangeReadyForWrangler -->

[[Category:SelfContainedChange]]

* Targeted release: [[Releases/34 | Fedora 34 ]]
* Last updated: <!-- this is an automatic macro — you don't need to change this line -->  {{REVISIONYEAR}}-{{REVISIONMONTH}}-{{REVISIONDAY2}}
* FESCo issue: [https://pagure.io/fesco/issue/2533 #2533]
* Tracker bug: [https://bugzilla.redhat.com/show_bug.cgi?id=1913853 #1913853]
* Release notes tracker:[https://pagure.io/fedora-docs/release-notes/issue/632 #632]

== Detailed Description ==
The Ruby on Rails stack is evolving quickly and Fedora needs to keep pace with it. Therefore the whole Ruby on Rails stack should be updated from 6.0 in Fedora 33 to 6.1 (latest version) in Fedora 34. This will ensure that all the Ruby developers using Fedora have the latest and greatest RPM-packaged Ruby on Rails.

== Benefit to Fedora ==
This update will keep Fedora up-to-date and will ensure that the current Ruby on Rails developers stay with us as they will get support for system-packaged Ruby on Rails of the latest version. Apart from that, update to Rails 6.1 will bring Horizontal Sharding, Multi-DB Improvements, Strict Loading, Destroy Associations in Background, Error Objects and more. Update to Rails 6.1 contains hundreds of other fixes and improvements across all the frameworks.

== Scope ==
* Proposal owners:
** The whole Rails stack has to be updated.
** Some dependencies of the Rails stack will need update.

=== Packages need to be created/updated ===

{|
! Package name
! Task
! Bug
! Pull Request
|-
|rubygem-actioncable
|Update to 6.1.x
|[https://bugzilla.redhat.com/show_bug.cgi?id=1906179 #1906179]
|[https://src.fedoraproject.org/rpms/rubygem-actioncable/pull-request/2 PR]
|-
|rubygem-actionmailbox
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-actionmailbox/pull-request/1 PR]
|-
|rubygem-actionmailer
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-actionmailer/pull-request/2 PR]
|-
|rubygem-actionpack
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-actionpack/pull-request/2 PR]
|-
|rubygem-actiontext
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-actiontext/pull-request/1 PR]
|-
|rubygem-actionview
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-actionview/pull-request/2 PR]
|-
|rubygem-activejob
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-activejob/pull-request/2 PR]
|-
|rubygem-activemodel
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-activemodel/pull-request/2 PR]
|-
|rubygem-activerecord
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-activerecord/pull-request/3 PR]
|-
|rubygem-activestorage
|Update to 6.1.x
|[https://bugzilla.redhat.com/show_bug.cgi?id=1906180 #1906180]
|[https://src.fedoraproject.org/rpms/rubygem-activestorage/pull-request/3 PR]
|-
|rubygem-activesupport
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-activesupport/pull-request/3 PR]
|-
|rubygem-rails
|Update to 6.1.x
|[https://bugzilla.redhat.com/show_bug.cgi?id=1906183 #1906183]
|[https://src.fedoraproject.org/rpms/rubygem-rails/pull-request/2 PR]
|-
|rubygem-railties
|Update to 6.1.x
|N/A
|[https://src.fedoraproject.org/rpms/rubygem-railties/pull-request/2 PR]
|}
Current development state can be observed in [https://copr.fedorainfracloud.org/coprs/pvalena/ruby-on-rails/ pvalena/ruby-on-rails] COPR repository. 
* Other developers: Update Rails dependent packages to be working with Ruby on Rails 6.1 <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
* Release engineering: [https://pagure.io/releng/issue/9918 #9918]<!-- REQUIRED FOR SYSTEM WIDE AS WELL AS FOR SELF CONTAINED CHANGES -->

* Policies and guidelines: N/A (not a System Wide Change) <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
* Trademark approval: N/A (not needed for this Change)

== Upgrade/compatibility impact ==
Web applications build above Ruby on Rails framework might need to be updated. Official upstream upgrade guide might come handy:
http://guides.rubyonrails.org/upgrading_ruby_on_rails.html

== How To Test ==
* No special hardware is needed.

=== To test Rails 6.1 from upstream ===
<pre>
gem install rails -v 6.1.x
rails new app
cd app && rails s
</pre>
* Go to http://127.0.0.1:3000/ and make sure you are running Rails 6.1.x

=== To test only Rails itself ===
<pre>
dnf install rubygem-rails
rails new app
cd app && rails s
</pre>
* Go to http://127.0.0.1:3000/ and make sure you are running Rails 6.1.x

=== To test the complete feature including generating a new Rails app using RPM ===
<pre>
dnf group install 'Ruby on Rails'
rails new app --skip-bundle && cd app
rails s
</pre>
* Go to http://127.0.0.1:3000/ and make sure you are running Rails 6.1.x

== User Experience ==
* New version of Ruby on Rails (6.1) available
* The most significant Rails 6.1 features:
** Multi-DB Improvements
** Horizontal Sharding
** Strict Loading Associations
** Delegated Types
** Destroy Associations Async
** Error Objects
** Active Storage Improvements
** Disallowed Deprecation Support
* Please also note:
** The classic Autoloader is Deprecated

== Dependencies ==
* There are several packages, which depends on Ruby on Rails framework.
* These needs to be surely updated:
** (none)
* Following gems don't support Rails 6.1 right now and would be broken by the update:
** (none)
* As Rails requires Ruby >= 2.5, the platform less than the version can not use Rails 6.1.

== Contingency Plan ==
* Contingency mechanism: None needed. Rails stack won't be updated until all its dependencies are in Rawhide. After that, it will be a simple matter of updating the core packages (and their dependencies).  <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
* Contingency deadline: N/A (not a System Wide Change)  <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
* Blocks release? No <!-- REQUIRED FOR SYSTEM WIDE CHANGES -->
* Blocks product? No <!-- Applicable for Changes that blocks specific product release/Fedora.next -->

== Documentation ==
* http://api.rubyonrails.org/

== Release Notes ==
* https://edgeguides.rubyonrails.org/6_1_release_notes.html
* https://weblog.rubyonrails.org/2020/12/9/Rails-6-1-0-release/
