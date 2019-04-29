EXTRA_DIST = do-tests make-testing ssh start-testing stop-testing \
             testing.conf ssh_config config hosts images scripts tests \
			 README

# exclude all files ignored by Git from the tarball
dist-hook:
	find hosts tests -print0 | \
		git -C $(srcdir) check-ignore -z --stdin --no-index | \
		xargs -0 -I{} rm -rf $(distdir)/{}
