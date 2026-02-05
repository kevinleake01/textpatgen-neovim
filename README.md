# Textpatgen-Neovim

Textpatgen-Neovim is a program that uses the Text Pattern Generator in NeoVim.<br>

To get started, go into 01-workspace and you will see a list of template files<br>
written in Lua. This is tpl-0001.lua:<br>

<pre>
-- TEXTPATGEN-NEOVIM LUA SCRIPT
-- Please edit this file to suit your preferences.
-- The text is written to a timestamped file.

filename = os.date("00_%Y%m%d_%H%M%S.txt")
file = io.open(filename, "w")
introstr = os.date("TEXTPATGEN-NEOVIM: %Y-%m-%dT%H:%M:%S%z\n")
file:write(introstr)
n3 = 0
for n1 = 0, 15 do
  for n2 = 0, 14 do
    str = string.format("X-%04X ", n3)
    file:write(str)
    n3 = n3 + 1
    end 
  str = string.format("X-%04X\n", n3)
  file:write(str)
  n3 = n3 + 1
end
file:close()
</pre>

Let's open this in NeoVim with this command:<br>

<pre>
$ nvim tpl-0001.lua
</pre>

You can now edit this file to suit your preferences. To save the file, use this command:<br>

<pre>
:w
</pre>

Now we will run this file to get the generated text, by doing this:<br>

<pre>
:source tpl-0001.lua
</pre>

The generated text will be saved to a named timestamped file, and you should see something<br>
like this:<br>

<pre>
</pre>

You can now edit this new timestamped file in NeoVim by using this command:<br>

<pre>
:e 
</pre>

NeoVim does many other things. To see more about NeoVim, take a look at<br>
html5-bookmarks-neovim.html<br>
<br>
<br>


