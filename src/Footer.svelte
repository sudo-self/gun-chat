<footer>
  Made with
  <span>♥️</span>
  by
  <a href="https://jessejesse.com">sudo-self</a>
  <br />
  Using
  <a href="https://svelte.dev/">svelte</a>
  and
  <a href="https://gun.eco/">gunData</a>
  see
  <a href="https://github.com/sudo-self">Github</a>
  <br />
  v. {process.env.APP_VERSION} git {process.env.COMMIT_HASH}
</footer>

<style>
  footer {
    color: grey;
    margin: 4rem 0 1rem 0;
    font-size: 10px;
    text-align: center;
    line-height: 1.6;
  }

  span {
    color: red;
  }
</style>
