function buildExamples (data) {
 const content = document.getElementById('content')
 const titles = ["Ryhthmus","Begleitung","Melodie"]
 for (let i = 0; i < data.length; i++) {
   const row = document.createElement('div')
   row.classList.add('row')
   const h5 = document.createElement('h5')
   h5.innerHTML = data[i].title
   row.appendChild(h5)
   const ul = document.createElement('ul')
   ul.classList.add("collapsible")
   for (let j = 0, a = 0; j < data[i].snippets.length/3; j++,a+=3) {
     ul.appendChild(createListElements(
      data[i].snippets[a],
      data[i].snippets[a+1],
      data[i].snippets[a+2],
      titles[j]
     ))
   }
   row.appendChild(ul)
   content.appendChild(row)
 }
}

function createListElements (s1,s2,s3,t) {
  const li = document.createElement('li')
  const title = document.createElement('div')
  title.classList.add('collapsible-header')
  title.innerHTML = t
  li.appendChild(title)

  const liContent = document.createElement('div')
  liContent.classList.add("collapsible-body")
  liContent.classList.add("col-body")

  if (s1) liContent.appendChild(createExample(s1))
  if (s2) liContent.appendChild(createExample(s2))
  if (s3) liContent.appendChild(createExample(s3))

  li.appendChild(liContent)
  return li
}

function stopAllAudio () {
  if (currentAudio) {
      currentAudio.pause()
      currentAudio.currentTime = 0.0
  }
}

let currentAudio = null
function createExample (snippet) {
 const div = document.createElement('div')
 div.classList.add('rel')
 div.classList.add('col')
 div.classList.add('s12')
 div.classList.add('m4')

 const copyBtn = document.createElement('a')
 copyBtn.classList.add('btn-copy')
 copyBtn.classList.add('waves-effect')
 copyBtn.classList.add('waves-light')
 copyBtn.classList.add('btn-small')
 copyBtn.innerHTML = '<i class="material-icons">content_copy</i>'
 copyBtn.addEventListener('click',() => {
   copyCodeSnippet(snippet.code)
   M.toast({html: 'Snippet kopiert!'})
 })

 const playBtn = document.createElement('a')
 playBtn.classList.add('btn-play-snippet')
 playBtn.classList.add('btn-floating')
 playBtn.classList.add('btn-large')
 playBtn.classList.add('waves-effect')
 playBtn.classList.add('waves-light')
 playBtn.classList.add('red')
 playBtn.innerHTML = '<i class="material-icons">play_arrow</i>'
 playBtn.addEventListener('click',() => {
   stopAllAudio()
   currentAudio = new Audio('files/'+snippet.filename)
   currentAudio.play()
 })

 const pre = document.createElement('pre')
 pre.innerHTML = snippet.code
 const wrapper = document.createElement('div')
 wrapper.classList.add('rel')
 wrapper.appendChild(copyBtn)
 wrapper.appendChild(playBtn)
 wrapper.appendChild(pre)
 const h6 = document.createElement('h6')
 h6.classList.add('code-title')
 h6.innerHTML = snippet.name || ""
 div.appendChild(wrapper)
 div.appendChild(h6)

 return div
}




function copyCodeSnippet (copyText) {
  const textArea = document.createElement('textarea');
  textArea.textContent = copyText;
  document.body.append(textArea);
  textArea.select();
  document.execCommand("copy");
  textArea.remove()
}

function SonicPiSyntaxHighlighter () {
  const self = this

  this.reg0 = /(\:\w*)/g
  this.reg1 = /(\w*\.\w*)/g
  this.reg2 = /\b(if|end|do|while|nil|false|true)(?=[^\w])/g
  this.reg3 = /(\d|times)/g
  this.reg4 = /(#.*)/gm

  this.init = function () {
    var matches = document.querySelectorAll('pre')
    for (var i = 0; i < matches.length; i++) {
      self.highlight(matches[i])
    }
  }

  this.highlight = function (elem) {
   var text = elem.innerHTML
   var parsed = ""

   parsed = text.replace(self.reg0,'<span class="doublePoint">$1</span>')
   parsed = parsed.replace(self.reg2,'<span class="keywords">$1</span>')
   parsed = parsed.replace(self.reg3,'<span class="dot">$1</span>')
   parsed = parsed.replace(self.reg4,'<span class="comment">$1</span>')

   elem.innerHTML = parsed
  }

}

window.addEventListener('DOMContentLoaded',() => {
 buildExamples(data)
 var elems = document.querySelectorAll('.collapsible');
 var instances = M.Collapsible.init(elems);

 new SonicPiSyntaxHighlighter().init()
})
