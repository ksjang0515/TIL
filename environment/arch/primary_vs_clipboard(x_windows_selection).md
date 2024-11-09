# Primary vs Clipboard (X Windows Selection)

The data transfer method is divided into two, passive and active, depending on the participation of the sender during transfer [[1]](https://en.wikipedia.org/wiki/X_Window_selection#Active_and_passive_selections).

- Active (Drag-and-drop). Sender participates on transfer. Can divide large data into smaller parts and transfer as series of sequential transfers. Once the sender has been terminated, transfer can't be made. Sender and receiver can negotiate to convert data into suitable form before transfer.
- Passive (Cut buffer). Once the data is selected, it is stored elsewhere, therefore the sender doesn't participate on transfer. As it is stored in another storage, all data has to be stored and transfer can be made even after the sender has been terminated. Data format can't be converted.

Two selections that are standardized and frequently used are Primary Selection and Clipboard. Primary Selection occurs when the text has been selected(highlighted) and middle click is used to paste. Clipboard uses explicit copy and paste command [[2]](https://unix.stackexchange.com/questions/139191/whats-the-difference-between-primary-selection-and-clipboard-buffer_).

At the base level, primary and clipboard are identical thus nothing is copied until it is pasted, only the ownership is granted and once the sender has been terminated, the data is lost. This is shown when copying text on the terminal then closing the terminal, paste command pastes nothing [[3]](https://unix.stackexchange.com/questions/213840/how-to-toggle-or-turn-off-text-selection-being-sent-to-the-clipboard/213843#213843).

Xclipboard modifies this behavior and makes the clipboard to transfer data into the buffer on copy, creating the behavior that we are familiar, making clipboard be passive. Note, ownership is granted on copy due to memory isolation by operating system [[4]](https://en.wikipedia.org/wiki/X_Window_selection#Clipboard).
