# Abacus Activity Flatpak

Abacus is a tool for simple arithmetic calculations.

To know more refer https://github.com/flathub/org.sugarlabs.AbacusActivity

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.AbacusActivity.git
cd org.sugarlabs.AbacusActivity
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.AbacusActivity.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.AbacusActivity
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.AbacusActivity.json
```