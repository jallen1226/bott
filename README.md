const puppeteer = require('puppeteer');

const rand_url = "https://www.footlocker.com/en/product/~/D1391101.html"

async function initBroswer(){
  const browser = await puppeteer.launch({headless: false});
  const page = await browser.newPage();
  await page.goto(rand_url);
  return page;
