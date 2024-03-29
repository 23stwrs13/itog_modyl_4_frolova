<div class="container">
      <h1>Фильм порядок показа</h1>
      <button id="addButton">Фильм открыть</button>
      <div id="filmsList">
      </div>
      <script>
      document.addEventListener('DOMContentLoaded', function() {
        let films = [
        { title: 'Онегин', ganr: 'Мелодрама' },
        { title: 'Материнский инстинкт', ganr: 'Психологический триллер' },
        { title: 'Уиджи. Потустороннее измерение', ganr: 'Хоррор' },
        { title: 'Ненормальный', ganr: 'Драма, комедия' },
        { title: 'Омен. Непорочная', ganr: 'Хоррор' }];
        let addButton = document.getElementById('addButton');
        let filmsList = document.getElementById('filmsList');
        
        addButton.addEventListener('click', function() {
        let film = films[Math.floor(Math.random() * 10)];
        let filmElement = document.createElement('div');
        filmElement.classList.add('film');
        
        let titleElement = document.createElement('h2');
        titleElement.textContent = film.title;
        filmElement.appendChild(titleElement);
        
        let ganrElement = document.createElement('p');
        ganrElement.textContent = 'Жанр: ' + film.ganr;
        filmElement.appendChild(ganrElement);
        
        filmsList.appendChild(filmElement);
        });
        });     
      </script>   
</div>