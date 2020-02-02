# emoji-cheat-sheet-plus :+1:

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc/generate-toc again -->
**Table of Contents** :blue_book:

- [emoji-cheat-sheet-plus](#emoji-cheat-sheet-plus)
    - [What's new in this fork ?](#whats-new-in-this-fork-)
    - [Using emoji-cheat-sheet-plus](#using-emoji-cheat-sheet-plus)
    - [License](#license)

<!-- markdown-toc end -->

## What's new in this fork ? :fork_and_knife:

This work is based on the work of [Shingo Fukuyama][upstream].

This fork proposes the following additional feature:

- emoji buffer has its own major-mode,
- automatic display of emoji code in the minibuffer while browsing the
  emoji buffer,
- new minor mode: `emoji-cheat-sheet-plus-display-mode` replacing emoji codes
  in buffer by the its image,
- new function: `emoji-cheat-sheet-plus-insert` to insert an emoji at point
  using an helm front-end. It is possible to insert several emoji thanks
  to helm persistent action or its multiple selection feature.

## Using emoji-cheat-sheet-plus :electric_plug:

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

## License :copyright:

This project is licensed under GPL v3.

Images are from [arvida/emoji-cheat-sheet.com][]

- `octocat`, `squirrel`, `shipit`
  Copyright (c) 2012 GitHub Inc. All rights reserved.
- `bowtie`
  Copyright (c) 2012 37signals, LLC. All rights reserved.
- `neckbeard`
  Copyright (c) 2012 Jamie Dihiansan. Creative Commons Attribution 3.0 Unported
- `feelsgood`, `finnadie`, `goberserk`, `godmode`, `hurtrealbad`, `rage 1-4`, `suspect`
  Copyright (c) 2012 id Software. All rights reserved.
- `trollface`
  Copyright (c) 2012 whynne@deviantart. All rights reserved.
- All other emoji images
  Copyright (c) 2012 Apple Inc. All rights reserved.

[upstream]: https://github.com/ShingoFukuyama/emacs-emoji-cheat-sheet
[arvida/emoji-cheat-sheet.com]: https://github.com/arvida/emoji-cheat-sheet.com
