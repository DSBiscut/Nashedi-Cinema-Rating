# Nashedi-Cinema-Rating

            <input type="radio" id="star1" name="rating" value="1"><label for="star1">★</label>
        </div>

        <div id="status"></div>

        <button class="btn-reset" onclick="resetRating()">Clear Rating</button>
    </div>

    <script>
        const stars = document.querySelectorAll('input[name="rating"]');
        const status = document.getElementById('status');

        stars.forEach(star => {
            star.addEventListener('change', () => {
                let val = star.value;
                if(val == 5) status.textContent = "Full Nashe! ⭐⭐⭐⭐⭐";
                else if(val == 4) status.textContent = "Badiya Tha! ⭐⭐⭐⭐";
                else if(val == 3) status.textContent = "Theek-Thak! ⭐⭐⭐";
                else if(val == 2) status.textContent = "Mazaa nahi aaya! ⭐⭐";
                else status.textContent = "Bilkul bakwas! ⭐";
                
                status.style.color = "#ffcc00";
            });
        });

        function resetRating() {
            stars.forEach(s => s.checked = false);
            status.textContent = "";
        }
    </script>

</body>
</html>
