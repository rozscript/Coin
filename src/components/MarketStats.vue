<script setup lang="ts">
import{
    BarChart3,
    CircleDollarSign,
    TrendingUp,
    Zap
}from 'lucide-vue-next'
</script>

<template>
    <section class="stats-grid">
      <article class="stas-card">
        <div class="stat-card-top">
            <div class="stat-icon">
                <CircleDollarSign :size="20"/>
            </div>

            <span class="stat-label">
                Total Market Cap 
            </span>

        </div>

        <div class="stat-value">
            $20T
        </div>

        <div class="stat-bottom">
            <span class="postive">
                <TrendingUp :size="14"/>
                +3.85%
            </span>

            <span class="stat-period">
                24h
            </span>
        </div>
      </article>

      <article class="stat-cars">
        <div class="stat-card-top">
            <div class="stat-icon">
                <BarChart3 :size="20"/>
            </div>
           
        <span class="stat-label">
            BTC Dominance
        </span>    
        </div>
        
        <div class="stat-value">
            55%
        </div>

        <div class="stat-bottom">
            <span class="positive">
                <TrendingUp :size="14"/>
                0.40%
            </span>

            <span class="stat-period">
                24h
            </span>
        </div>
      </article>

      <article class="stat-card">
        <div class="stat-card-top">
            <div class="stat-icon">
                <Zap :size="20"/>
            </div>

            <span class="stat-label">
                Market Sentiment
            </span>
        </div>

        <div class="stat-value">
            72
            <span class="stat-unit">
                / 100
            </span>
        </div>

        <div class="stat-bottom">
            <span class="sentiment">
                Greed
            </span>

            <span class="stat-period">
                Fear & Greed
            </span>
        </div>
      </article>

    
    </section>
</template>