# telopi-deploy-test

This is a test repo for Telopi's deploy events. It holds nothing real and is
safe to delete.

`shop/` is a small three-deployment shop (`checkout`, `payments`, `frontend`)
that an Argo CD Application syncs into the `shop` namespace of a laptop test
cluster. Changing `PAYMENTS_URL` of `checkout` from port 8080 (healthy) to
8081 makes `checkout` crash-loop, so a commit here is a deploy that breaks
something, and Argo CD's notifications can tell Telopi about it.

Keep `main` on 8080 (healthy) between tests.
