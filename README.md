# emoji-cheat-sheet-plus

## What's new in this fork ?

This work is based on the work of [Shingo Fukuyama][upstream].

This fork proposes the following additional feature:

- emoji buffer has its own major-mode,
- automatic display of emoji code in the minibuffer while browsing the
  emoji buffer,
- new minor mode: `emoji-cheat-sheet-plus-display-mode` replacing emoji codes
  in buffer by the its image,
- new function: `emoji-cheat-sheet-plus-insert` to insert an emoji at point
  using an helm front-end. It is the possible to insert several emoji thanks
  to helm persistent action or its multiple selection feature.

## Using emoji-cheat-sheet-plus

```elisp
(use-package emoji-cheat-sheet-plus
    :defer t
    :init
    (progn
      ;; enabled emoji in buffer
      (add-hook 'org-mode-hook 'emoji-cheat-sheet-plus-display-mode)
      ;; insert emoji with helm
      (global-set-key (kbd "C-c C-e") 'emoji-cheat-sheet-plus-insert)))
```

You can open a dedicated buffer to browse for emoji with
`M-x emoji-cheat-sheet-plus-buffer`.

[upstream]: https://github.com/ShingoFukuyama/emacs-emoji-cheat-sheet
