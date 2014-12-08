;; Turn on font lock mode every time Emacs initializes a buffer 

;; for Lisp or C.

;;

(setq-default indent-tabs-mode nil)
(setq-default tab-width 4)
(setq indent-inline-function 'insert-tab)

(ido-mode 1)
(electric-pair-mode 1)
(add-hook 'emacs-lisp-mode-hook 'turn-on-font-lock)

(add-hook 'c-mode-hook 'turn-on-font-lock)

(transient-mark-mode 1) ; highlight text selection
(delete-selection-mode 1) ; delete seleted text when typing


;(global-font-lock-mode 1) ; turn on syntax coloring



(add-to-list 'load-path  "~/emacs.d/cedet")


(load-file "/users/chbin/emacs.d/cedet/common/cedet.el")

(require 'cedet)
(require 'semantic-ia)
 
;; Enable EDE (Project Management) features
(global-ede-mode 1)
 
(semantic-load-enable-excessive-code-helpers)
(semantic-load-enable-semantic-debugging-helpers)
 
;; Enable SRecode (Template management) minor-mode.
(global-srecode-minor-mode 1)

(add-to-list 'load-path "/users/chbin/emacs.d/ecb")
(load-file "/users/chbin/emacs.d/ecb/ecb.el")

;;(add-to-list 'load-path "/users/chbin/emacs.d/ecb-new/ecb/ecb")
;;(load-file "/users/chbin/emacs.d/ecb-new/ecb/ecb/ecb.el")


(require 'ecb-autoloads)
(setq stack-trace-on-error nil)
(setq ecb-tip-of-the-day nil)
(setq ecb-examples-bufferinfo-buffer-name nil)

(load-file "/users/chbin/emacs.d/cscope-15.8a/contrib/xcscope/xcscope.el")
(require 'xcscope)
(setq cscope-do-not-update-database t)


(semanticdb-enable-cscope-databases)
(custom-set-variables
 ;; custom-set-variables was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 '(ansi-color-faces-vector [default bold shadow italic underline bold bold-italic bold])
 '(ansi-color-names-vector (vector "#ffffff" "#bf616a" "#B4EB89" "#ebcb8b" "#89AAEB" "#C189EB" "#89EBCA" "#232830"))
 '(custom-safe-themes (quote ("7f14fad67d7ac8d0555bd5a1fd1a429ce2dd37162c4e2dc7ae501f54bad1273a" "0e121ff9bef6937edad8dfcff7d88ac9219b5b4f1570fd1702e546a80dba0832" "f0a99f53cbf7b004ba0c1760aa14fd70f2eabafe4e62a2b3cf5cabae8203113b" "628278136f88aa1a151bb2d6c8a86bf2b7631fbea5f0f76cba2a0079cd910f7d" "1b8d67b43ff1723960eb5e0cba512a2c7a2ad544ddb2533a90101fd1852b426e" "82d2cac368ccdec2fcc7573f24c3f79654b78bf133096f9b40c20d97ec1d8016" "bb08c73af94ee74453c90422485b29e5643b73b05e8de029a6909af6a3fb3f58" "bd115791a5ac6058164193164fd1245ac9dc97207783eae036f0bfc9ad9670e0" default)))
 '(ecb-options-version "2.40")
 '(fci-rule-color "#343d46")
 '(jde-ant-buildfile "./build.xml")
 '(jde-ant-read-target t)
 '(jde-ant-working-directory "")
 '(jde-build-function (quote jde-ant-build))
 '(jde-compiler (quote ("javac")))
 '(jde-global-classpath (quote ("." "classes" "lib" "src" "")))
 '(jde-jdk (quote ("1.6")))
 '(jde-jdk-registry (quote (("1.6" . "/Library/Java/JavaVirtualMachines/jdk1.7.0_51.jdk/Contents/Home"))))
 '(jde-sourcepath (quote ("./src" "./gen-java" "/Users/chbin/Tools/thrift-0.9.1/lib/java/src")))
 '(vc-annotate-background nil)
 '(vc-annotate-color-map (quote ((20 . "#bf616a") (40 . "#DCA432") (60 . "#ebcb8b") (80 . "#B4EB89") (100 . "#89EBCA") (120 . "#89AAEB") (140 . "#C189EB") (160 . "#bf616a") (180 . "#DCA432") (200 . "#ebcb8b") (220 . "#B4EB89") (240 . "#89EBCA") (260 . "#89AAEB") (280 . "#C189EB") (300 . "#bf616a") (320 . "#DCA432") (340 . "#ebcb8b") (360 . "#B4EB89"))))
 '(vc-annotate-very-old-color nil))
(custom-set-faces
 ;; custom-set-faces was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 )



(when (fboundp 'windmove-default-keybindings)
  (windmove-default-keybindings))

(windmove-default-keybindings 'meta)

;; (global-set-key (kbd "C-c <left>")  'windmove-left)
;; (global-set-key (kbd "C-c <right>") 'windmove-right)
;; (global-set-key (kbd "C-c <up>")    'windmove-up)
;; (global-set-key (kbd "C-c <down>")  'windmove-down)


(defun ignore-error-wrapper (fn)
  "Funtion return new function that ignore errors.
   The function wraps a function with `ignore-errors' macro."
  (lexical-let ((fn fn))
    (lambda ()
      (interactive)
      (ignore-errors
        (funcall fn)))))


(global-set-key [s-left] (ignore-error-wrapper 'windmove-left))
(global-set-key [s-right] (ignore-error-wrapper 'windmove-right))
(global-set-key [s-up] (ignore-error-wrapper 'windmove-up))
(global-set-key [s-down] (ignore-error-wrapper 'windmove-down))


(load-file "~/emacs.d/window-number.el")
(require 'window-number)
(window-number-mode 1)

(require 'linum)
(global-linum-mode 1)

;; (add-to-list 'load-path "/users/chbin/emacs.d/anything-config")
;; (require 'anything-config)

;;jdee
(add-to-list 'load-path "~/emacs.d/jdee-2.4.1/lisp")
(load "jde")

;;auto-complete-mode
(add-to-list 'load-path "/Users/chbin/emacs.d/")
(require 'auto-complete-config)
(add-to-list 'ac-dictionary-directories "/Users/chbin/emacs.d//ac-dict")
(ac-config-default)

;;melpa
(require 'package)
(add-to-list 'package-archives
             '("melpa" . "http://melpa.milkbox.net/packages/") t)
(when (< emacs-major-version 24)
  ;; For important compatibility libraries like cl-lib
  (add-to-list 'package-archives '("gnu" . "http://elpa.gnu.org/packages/")))
(package-initialize)

;;themes
(add-to-list 'custom-theme-load-path "~/emacs.d/themes")

(load-theme 'cyberpunk t)


(defun my-max-window()
(x-send-client-message nil 0 nil "_NET_WM_STATE" 32
'(2 "_NET_WM_STATE_MAXIMIZED_HORZ" 0))
(x-send-client-message nil 0 nil "_NET_WM_STATE" 32
'(2 "_NET_WM_STATE_MAXIMIZED_VERT" 0))
)
(run-with-idle-timer 1 nil 'my-max-window)


(fset 'chbin_first_macro
   [?\C-e ?- ?- ?f ?o ?o ?b ?a ?r ?  ?n ?e ?w ?  ?l ?i ?e backspace ?n ?e ?\C-a ?\C-n])


(load-file "~/emacs.d/doc-mode.el")
(require 'doc-mode)
(add-hook 'java-mode-hook 'doc-mode)

(global-set-key (kbd "C-c l") 'goto-line)

(add-to-list 'load-path "/Users/chbin/.emacs.d/elpa/helm-20140910.1226")
(require 'helm-config)

;; The default "C-x c" is quite close to "C-x C-c", which quits Emacs.
;; Changed to "C-c h". Note: We must set "C-c h" globally, because we
;; cannot change `helm-command-prefix-key' once `helm-config' is loaded.
(global-set-key (kbd "C-c h") 'helm-command-prefix)
(global-unset-key (kbd "C-x c"))

(define-key helm-map (kbd "<tab>") 'helm-execute-persistent-action) ; rebind tab to run persistent action
(define-key helm-map (kbd "C-i") 'helm-execute-persistent-action) ; make TAB works in terminal
(define-key helm-map (kbd "C-z")  'helm-select-action) ; list actions using C-z

(when (executable-find "curl")
  (setq helm-google-suggest-use-curl-p t))

(setq helm-split-window-in-side-p           t ; open helm buffer inside current window, not occupy whole other window
      helm-buffers-fuzzy-matching           t ; fuzzy matching buffer names when non--nil
      helm-move-to-line-cycle-in-source     t ; move to end or beginning of source when reaching top or bottom of source.
      helm-ff-search-library-in-sexp        t ; search for library in `require' and `declare-function' sexp.
      helm-scroll-amount                    8 ; scroll 8 lines other window using M-<next>/M-<prior>
      helm-ff-file-name-history-use-recentf t)

(helm-mode 1)


;; (global-set-key [(meta x)] (lambda ()
;;                              (interactive)
;;                              (or (boundp 'smex-cache)
;;                                  (smex-initialize))
;;                              (global-set-key [(meta x)] 'smex)
;;                              (smex)))

;; (global-set-key [(shift meta x)] (lambda ()
;;                                    (interactive)
;;                                    (or (boundp 'smex-cache)
;;                                        (smex-initialize))
;;                                    (global-set-key [(shift meta x)] 'smex-major-mode-commands)
;;                                    (smex-major-mode-commands)))
;;; Smex
(require 'smex) ; Not needed if you use package.el
(smex-initialize) ; Can be omitted. This might cause a (minimal) delay
                  ; when Smex is auto-initialized on its first run.
(autoload 'smex "smex"
  "Smex is a M-x enhancement for Emacs, it provides a convenient interface to
your recently and most frequently used commands.")


;; (global-set-key (kbd "M-x") 'smex)
;; (global-set-key (kbd "M-X") 'smex-major-mode-commands)
;; ;; This is your old M-x.
;; (global-set-key (kbd "C-c C-c M-x") 'execute-extended-command)

(global-set-key (kbd "M-x") 'helm-M-x)
