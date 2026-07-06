Docker leverages containers without any underlying virtual machine. Its
lightweight footprint makes is the preferred way for:

1. Exploring BOSH
2. Local release development,
3. Testing releases (local or in CI).

Behind the scenes, the BOSH Director uses Warden stemcells to deploy
containers, similar to the
legacy VirtualBox 
